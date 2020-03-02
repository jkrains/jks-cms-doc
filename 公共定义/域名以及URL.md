# 域名以及URL
| 域名                               | 说明                                               |
| ---------------------------------- | -------------------------------------------------- |
| ~~https://api.cms.jikeyiyong.com~~ | ~~企业内容管理平台API域名https协议（暂时不支持）~~ |
| http://api.cms.jikeyiyong.com      | 企业内容管理平台 API域名http协议                   |

# 系统URL定义
| 定义                    | 路径                   | 说明                                                         |
| ----------------------- | ---------------------- | ------------------------------------------------------------ |
| URL_PHONE_CAPTCHA       | "/phone-captcha"       | 获取手机验证码，支持登录，密码找回功能                       |
| URL_EMIAL_CAPTCHA       | "/email-captcha"       | 邮件验证码登录，支持登录，密码找回功能                       |
| URL_TOKEN               | "/token"               | 获取token接口，主要用于                                      |
| URL_LOGIN               | "/login"               | 用户名，手机号或者邮箱登录接口，只有认证过的邮箱或手机号支持登录 |
| URL_CAPTCHA_LOGIN       | "/captcha-login"       | 手机验证码登录接口，只有认证过的手机号码支持登录             |
| URL_LOGOUT              | "/logout"              | 退出登录， 清理服务器token等信息                             |
| URL_JOIN                | "/join"                | 注册接口                                                     |
| URL_PASSWORD_RESET      | "/password-reset"      | 重置密码                                                     |
| URL_ACCOUNT_EXISTED     | "/account/existed"     | 当前账户是否存在，【无需登录完全开放接口】                   |
|                         |                        |                                                              |
| URL_CLASSIFICATION      | "/classification"      | 获取分类信息                                                 |
| URL_TAG_INFO            | "/tag-info"            | 获取分组信息或标签信息                                       |
| URL_COS_CREDENTIALS     | "/cos-credentials/:id" | 获取对象存储访问凭证                                         |
| URL_APP_INFO            | "/app-info"            | 获取应用程序信息                                             |
| URL_BOOK_PAGES          | "/book-pages"          | 书籍页管理                                                   |
|                         |                        |                                                              |
| URL_SITES               | "/sites"               | 站点管理                                                     |
| URL_NAVS                | "/navs"                | 导航管理                                                     |
| URL_ARTICLES            | "/articles"            | 文章管理                                                     |
| URL_BOOKS               | "/books"               | 文集管理（书籍管理）                                         |
| URL_SLIDERS             | "/sliders"             | 轮播图管理                                                   |
| URL_TEXTS               | "/texts"               | 文本管理                                                     |
| URL_LABELS              | "/labels"              | 标签管理                                                     |
| URL_PICTURES            | "/pictures"            | 图片管理                                                     |
| URL_VIDEOS              | "/videos"              | 视频管理                                                     |
| URL_AUDIOS              | "/audios"              | 音频管理                                                     |
| URL_FILES               | "/files"               | 文件管理                                                     |
| URL_NEWS                | "/news"                | 图文消息管理                                                 |
| URL_PRODUCTS            | "/products"            | 商品管理                                                     |
|                         |                        |                                                              |
| URL_PAY_DINNER          | "/pay-dinner"          | 支付套餐接口                                                 |
| URL_VALUATION_DINNER    | "/valuation-dinner"    | 评估套餐价格接口                                             |
| URL_DINNERS             | "/dinners"             | cms套餐获取                                                  |
|  |  |  |
| URL_SITE_CORRELATION    | "/site-correlation"    | 站点关联信息获取                                             |
| URL_RES_CONFIG          | "/rconfig"             | 资源配置                                                     |
| URL_WECHAT_ACCESS_TOKEN | "/watoken"             | 微信访问token                                                |
| URL_WECHAT_BUTTON_EXTRA | "/wbtn-extra""         | 微信菜单按钮额外信息                                         |
| URL_WECHAT_REF_MSG      | "/wref-msg"            | 微信引用消息                                                 |
|  |  |  |
| URL_SECRET_KEY          | "/secret-key"          | 访问密钥管理                                                 |
| URL_ACCESS_USER | "/access-user" | 访问子账号管理 |
| URL_ROLE_PERMISSION | "/role-permission" | 角色权限 |
| URL_USER_ROLE_CORRELATION | "/user-role-correlation" | 用户权限 |
| URL_USER_ROLE_CORRELATION | "/user-role-correlation" | 用户角色关联 |
| URL_PHONE_AUTHRZ | "/phone-authrz" | 短信验证码授权 |
| URL_EMAIL_AUTHRZ | "/email-authrz" | 邮件验证码授权 |
| URL_MATERIAL_COPY | "/material-cp"           | 素材拷贝 |
| URL_MATERIAL_MV | "/material-mv" | 素材移动 |

