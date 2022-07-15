# buession-springboot-pac4j 参考手册


## 配置属性


#### 通用配置

|  属性   | 类型   | 默认值    | 说明    |
|  ----  | ----   | ----     | ----   |
| spring.pac4j.clients                      | Set<String>                                  | --      | 启用认证的客户端类型名称，需要和各配置 [BaseConfig.BaseClientConfig](/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/BaseConfig.BaseClientConfig.html) 类型中的名称保持一致     |
| spring.pac4j.default-client               | String                                 | --      | 默认客户端类型名称     |
| spring.pac4j.ajax-request-resolver-class  | Class<? extends org.pac4j.core.http.ajax.AjaxRequestResolver>                                  | com.buession.security.pac4j.http.JsonAjaxRequestResolver      |  Compute if a HTTP request is an AJAX one and the appropriate response.     |
| spring.pac4j.multi-profile                | boolean                                | false      | 是否允许多个 Profile     |
| spring.pac4j.save-in-session              | boolean                                | true   | 是否保存到 SESSION 中     |


#### 客户端配置

##### CAS 配置


1. spring.pac4j.client.cas.proxy.enabled：表示 pac4j `CasConfiguration` 是否启用 `CasProxyReceptor`

详细配置参考 [https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/Cas.html](https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/Cas.html)


##### HTTP 配置

详细配置参考 [https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/Http.html](https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/Http.html)


##### JWT 配置

详细配置参考 [https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/Jwt.html](https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/Jwt.html)


##### OAuth 配置

详细配置参考 [https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/OAuth.html](https://springboot.buession.com/manual/2.0/docs/buession-springboot-pac4j/com/buession/springboot/pac4j/config/OAuth.html)

* 注：每类客户端均有 `enabled` 属性（如：spring.pac4j.client.cas.enabled），默认值为：false，表示是否启用该类客户端；每个客户端均有 `enabled` 属性（如：spring.pac4j.client.jwt.header.enabled），默认值为：false，表示是否启用该客户端.