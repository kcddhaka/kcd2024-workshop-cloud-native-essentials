
# Install Fluent-bit

```bash
# helm repo add fluent-bit https://fluent.github.io/helm-charts
helm repo add fluent https://fluent.github.io/helm-charts
```

Check possible value file:
```bash
helm show values fluent/fluent-bit
```

Specially output section:
```yaml
...
  inputs: |
    [INPUT]
        Name tail
        Path /var/log/containers/*.log
        Exclude_Path     /var/log/containers/*fluent-bit*.log,*.gz,*.zip
        multiline.parser docker, cri
        Tag kube.*
        Mem_Buf_Limit 50MB
        Skip_Long_Lines Off
        Refresh_Interval 10
        Rotate_Wait 30
        Buffer_Max_Size     4MB
        Buffer_Chunk_Size   2MB
...
  outputs: |
    [OUTPUT]
        Name es
        Match kube.*
        Host xxx.xxx.xxx.xxx
        Port 9200
        tls on
        tls.verify off
        HTTP_User elastic
        HTTP_Passwd xxxxx
        Logstash_Format On
        Logstash_Prefix k8sdevcl
        Retry_Limit False
        Replace_Dots  On
        Suppress_Type_Name On
        Trace_Error       On        

    [OUTPUT]
        Name es
        Match host.*
        Host xxx.xxx.xxx.xxx
        Port 9200
        tls on
        tls.verify off
        HTTP_User elastic
        HTTP_Passwd xxxx
        Logstash_Format On
        Logstash_Prefix k8sdevcl
        Retry_Limit False
        Replace_Dots  On
        Suppress_Type_Name On
        Trace_Error       On

...
```


Final command to install fluent-bit:
```bash
# final command to install
helm upgrade --install fluent-bit fluent/fluent-bit -f  fluent-bit-default-values.yaml

helm upgrade --install fluent-bit fluent/fluent-bit \
  -n fluent-bit --create-namespace \
  -f fluent-bit-default-values.yaml
```  



# References
