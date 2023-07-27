# clash-rules
clash-rules

# 
```yaml
proxy-providers:
# 从链接导入的配置文件（支持多个Clash 订阅链接）
 foo:
   type: http
   path: ./profiles/proxies/foo.yaml
   url: https://example-url (clash 订阅链接)
   interval: 3600 
   filter: 'Hong Kong' # 删选出含有该关键词的节点
   health-check:
     enable: true
     url: http://www.gstatic.com/generate_204
     interval: 300

 # 从本地导入的 clash 配置文件
 bar:
   type: file
   path: ./profiles/proxies/bar.yaml
   health-check:
     enable: true
     url: http://www.gstatic.com/generate_204
     interval: 600
```
