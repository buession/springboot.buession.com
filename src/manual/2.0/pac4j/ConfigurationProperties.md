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

|  属性   | 类型   | 默认值    | 说明    |
|  ----  | ----   | ----     | ----   |
| spring.pac4j.client.cas.enabled                           | boolean                            | false               | 是否启用 CAS 客户端     |
| spring.pac4j.client.cas.protocol                          | org.pac4j.cas.config.CasProtocol   | CasProtocol.CAS30   | 客户自定义属性     |
| spring.pac4j.client.cas.login-url                         | String                             | --                  | CAS 登录地址     |
| spring.pac4j.client.cas.prefix-url                        | String                             | --                  | CAS URL 前缀     |
| spring.pac4j.client.cas.callback-url                      | String                             | --                  | CAS 登录成功跳转地址     |
| spring.pac4j.client.cas.encoding                          | String                             | --                  | 编码     |
| spring.pac4j.client.cas.method                            | String                             | --                  | 请求方法     |
| spring.pac4j.client.cas.gateway                           | Boolean                            | --                  | Gateway     |
| spring.pac4j.client.cas.renew                             | Boolean                            | --                  | 是否重新认证     |
| spring.pac4j.client.cas.time-tolerance                    | Long                               | --                  |      |
| spring.pac4j.client.cas.post-logout-url-parameter         | String                             | --                  | 退出登录请求参数     |
| spring.pac4j.client.cas.custom-parameters                 | LinkedHashMap<String, String>      | --                  | 客户自定义参数     |
| spring.pac4j.client.cas.proxy.enabled                     | boolean                            | false               | 是否启用 CasProxyReceptor     |
| spring.pac4j.client.cas.general.enabled                   | boolean                            | false               | 是否启用常规 CAS 客户端     |
| spring.pac4j.client.cas.general.name                      | String                             | cas                 | 常规 CAS 客户端名称     |
| spring.pac4j.client.cas.general.custom-properties         | LinkedHashMap<String, Object>      | --                  | 常规 CAS 客户自定义属性     |
| spring.pac4j.client.cas.rest-form.enabled                 | boolean                            | false               | 是否启用常规 Cas Rest Form 客户端     |
| spring.pac4j.client.cas.rest-form.name                    | String                             | cas-rest-form       | Cas Rest Form 客户端名称    |
| spring.pac4j.client.cas.rest-form.username-parameter      | String                             | username            | Cas Rest Form 客户端用户名参数名称     |
| spring.pac4j.client.cas.rest-form.password-parameter      | String                             | password            | Cas Rest Form 客户端密码参数名称     |
| spring.pac4j.client.cas.rest-form.custom-properties       | LinkedHashMap<String, Object>      | --                  | Cas Rest Form 客户端客户自定义属性     |
| spring.pac4j.client.cas.direct.enabled                    | boolean                            | false               | 是否启用常规 Direct Cas Client 客户端     |
| spring.pac4j.client.cas.direct.name                       | String                             | direct-cas          | Direct Cas Client 客户端名称    |
| spring.pac4j.client.cas.direct.custom-properties          | LinkedHashMap<String, Object>      | --                  | Direct Cas Client 客户端客户自定义属性     |
| spring.pac4j.client.cas.direct-proxy.enabled              | boolean                            | false               | 是否启用常规 Direct Cas Proxy Client 客户端     |
| spring.pac4j.client.cas.direct-proxy.name                 | String                              | direct-cas-proxy   | Direct Cas Proxy Client 客户端名称     |
| spring.pac4j.client.cas.direct-proxy.custom-properties    | LinkedHashMap<String, Object>       | --                 | Direct Cas Proxy Client 客户自定义属性     |
| spring.pac4j.client.cas.rest-basic-auth.enabled           | boolean                             | false               | 是否启用常规 Cas Rest Basic Auth 客户端     |
| spring.pac4j.client.cas.rest-basic-auth.name              | String                              | cas-rest-basic-auth | Cas Rest Basic Auth 客户端名称    |
| spring.pac4j.client.cas.rest-basic-auth.header-name       | String                              | Authorization       | Cas Rest Basic Auth 客户端请求头名称    |
| spring.pac4j.client.cas.rest-basic-auth.prefix-header     | String                              | 'Basic '            | Cas Rest Basic Auth 客户端请求头前缀   |
| spring.pac4j.client.cas.rest-basic-auth.custom-properties | LinkedHashMap<String, Object>       | --                  | Cas Rest Basic Auth 客户自定义属性     |


##### HTTP 配置

|  属性   | 类型   | 默认值    | 说明    |
|  ----  | ----   | ----     | ----   |
| spring.pac4j.client.http.enabled                          | boolean                            | false               | 是否启用 HTTP 客户端     |
| spring.pac4j.client.http.callback-url                     | String                             | --                  | 登录成功跳转地址     |
| spring.pac4j.client.http.custom-parameters                | LinkedHashMap<String, String>      | --                  | 客户自定义参数     |
| spring.pac4j.client.http.form.enabled                     | boolean                            | false               | 是否启用 HTTP 表单客户端     |
| spring.pac4j.client.http.form.name                        | String                             | form                | HTTP 表单客户端名称     |
| spring.pac4j.client.http.form.username-parameter          | String                             | username            | HTTP 表单客户端用户名参数名称     |
| spring.pac4j.client.http.form.password-parameter          | String                             | password            | HTTP 表单客户端密码参数名称     |
| spring.pac4j.client.http.form.login-url          			| String                             | --                  | HTTP 表单客户端登录地址     |
| spring.pac4j.client.http.form.custom-properties           | LinkedHashMap<String, Object>      | --                  | HTTP 表单客户端客户自定义属性     |
| spring.pac4j.client.http.indirect-basic-auth.enabled      | boolean                            | false               | 是否启用 Indirect Basic Auth 客户端     |
| spring.pac4j.client.http.indirect-basic-auth.name         | String                             | indirect-basic-auth | Indirect Basic Auth 客户端名称     |
| spring.pac4j.client.http.indirect-basic-auth.custom-properties    | LinkedHashMap<String, Object>      | --                  | Indirect Basic Auth 客户端客户自定义属性     |
| spring.pac4j.client.http.direct-basic-auth.enabled        | boolean                            | false               | 是否启用 Direct Basic Auth 客户端     |
| spring.pac4j.client.http.direct-basic-auth.name           | String                             | direct-basic-auth | Direct Basic Auth 客户端名称     |
| spring.pac4j.client.http.direct-basic-auth.custom-properties    | LinkedHashMap<String, Object>      | --                  | Direct Basic Auth 客户端客户自定义属性     |

##### JWT 配置

|  属性   | 类型   | 默认值    | 说明    |
|  ----  | ----   | ----     | ----   |
| spring.pac4j.client.jwt.enabled                           | boolean                            | false               | 是否启用 JWT 客户端     |
| spring.pac4j.client.jwt.secret-signature-algorithm        | com.buession.springboot.pac4j.core.JWSAlgorithm   | JWSAlgorithm.HS256   | Secret 签名算法     |
| spring.pac4j.client.jwt.secret-encryption-algorithm       | com.buession.springboot.pac4j.core.JWEAlgorithm   | JWEAlgorithm.DIR   | Secret 加密算法     |
| spring.pac4j.client.jwt.encryption-method                 | com.buession.springboot.pac4j.core.EncryptionMethod  | EncryptionMethod.A128CBC_HS256                  | 加密算法     |
| spring.pac4j.client.jwt.encryption-key                    | String                             | --                  | 加密 Key     |
| spring.pac4j.client.jwt.identifier-generator              | Class<org.pac4j.core.util.generator.ValueGenerator>                             | --                  | 标识符生成器     |
| spring.pac4j.client.jwt.support-get-request               | boolean                            | false                  | 是否支持 GET 请求     |
| spring.pac4j.client.jwt.support-post-request              | boolean                            | true                | 是否支持 POST 请求     |
| spring.pac4j.client.jwt.custom-parameters                 | LinkedHashMap<String, String>      | --                  | 客户自定义参数     |
| spring.pac4j.client.jwt.header.enabled                    | boolean                            | false               | 是否启用 Jwt 请求头模式配置     |
| spring.pac4j.client.jwt.header.name                       | String                             | jwt-header          | Jwt 请求头模式客户端名称     |
| spring.pac4j.client.jwt.header.header-name                | String                             | ''                  | Jwt 请求头模式客户端请求头名称    |
| spring.pac4j.client.jwt.header.prefix-header              | String                             | ''                  | Jwt 请求头模式客户端请求头前缀   |
| spring.pac4j.client.jwt.header.custom-properties          | LinkedHashMap<String, Object>      | --                  | Jwt 请求头模式客户自定义属性     |
| spring.pac4j.client.jwt.cookie.enabled                    | boolean                            | false               | 是否启用 Jwt Cookie 模式配置     |
| spring.pac4j.client.jwt.cookie.name                       | String                             | jwt-cookie          | Jwt Cookie 模式客户端名称     |
| spring.pac4j.client.jwt.cookie.cookie-name                | String                             | ''                  | Jwt Cookie 模式客户端请求头名称    |
| spring.pac4j.client.jwt.cookie.custom-properties          | LinkedHashMap<String, Object>      | --                  | Jwt Cookie 模式客户自定义属性     |
| spring.pac4j.client.jwt.parameter.enabled                 | boolean                            | false               | 是否启用 Jwt 参数模式配置     |
| spring.pac4j.client.jwt.parameter.name                    | String                             | jwt-parameter       | Jwt 参数模式客户端名称     |
| spring.pac4j.client.jwt.parameter.parameter-name          | String                             | ''                  | Jwt 参数模式客户端请求头名称    |
| spring.pac4j.client.jwt.parameter.custom-properties       | LinkedHashMap<String, Object>      | --                  | Jwt 参数模式客户自定义属性     |