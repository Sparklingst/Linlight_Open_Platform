#粼光开放平台
# Linlight_Open_Platform
## 数据库数据说明
### `app_data`表

## 接口调用手册
### 获取应用数据
#### 调用地址
```
api/api_getAppData_AppId.php
```
#### 参数传递
| 传入参数 | 传入方式 | 是否必须 | 数据类型 | 备注 |
| ---- | ---- | ---- | ---- | ---- |
| AppId | POST | 是 | int | 应用在数据库中的序列标识 |
#### 返回值
| 返回参数 | 数据类型 | 备注 |  |
| ---- | ---- | ---- | ---- |
| code | int | 获取成功为1，不成功为非1 |  |
| message | string |  |  |
| data | array | 获取到应用的信息 |  |

#### 调用示例

**构造链接：** 
```
api/api_getAppData_AppId.php?AppId=1
```
**返回数据**：
``` PHP
Array
(
    [code] => 1
    [data] => Array
        (
            [0] => Array
                (
                    [AppId] => 1
                    [AppName] => 粼光
                    [AppDownloadUrl] => linlight.cn
                    [AppVersion] => 3.0
                    [AppNewVersion] => 3.0
                    [AppOneSentenceIntroduction] => 个人开发者交流平台
                    [AppIntroduction] => 粼光是一个基于个人应用分发的交流平台
                    [AppLogoUrl] => ./page/src/app_data/app_logo.png
                    [AppIntroductionPictureUrl] => 
                    [AppUpdateIntroduction] => 
                    [AppInerVersion] => 0
                    [AppUpUserId] => 0
                    [AppUniqueId] => 0
                    [AppType] => 
                )
        )
    [message] => Successful!
)
```

### 查询应用数据
#### 调用地址
```
api/api_searchApp_AppName.php
```
#### 参数传递
| 传入参数 | 传入方式 | 是否必须 | 数据类型 | 备注 |
| ---- | ---- | ---- | ---- | ---- |
| key | POST | 是 | string | 应用名称关键词，支持模糊包含关系的模糊搜索 |
#### 返回值
| 返回参数 | 数据类型 | 备注 |
| ---- | ---- | ---- |
| code | int | 获取成功为1，不成功为非1 |
| message | string |  |
| data | array | 获取到应用的信息 |

#### 调用示例

**构造链接：** 
```
api/api_searchApp_AppName.php?key=粼光
```
**返回数据**：
``` PHP
Array
(
    [code] => 1
    [data] => Array
        (
            [0] => Array
                (
                    [AppId] => 1
                    [AppName] => 粼光
                    [AppDownloadUrl] => linlight.cn
                    [AppVersion] => 3.0
                    [AppNewVersion] => 3.0
                    [AppOneSentenceIntroduction] => 个人开发者交流平台
                    [AppIntroduction] => 粼光是一个基于个人应用分发的交流平台
                    [AppLogoUrl] => ./page/src/app_data/app_logo.png
                    [AppIntroductionPictureUrl] => 
                    [AppUpdateIntroduction] => 
                    [AppInerVersion] => 0
                    [AppUpUserId] => 0
                    [AppUniqueId] => 0
                    [AppType] => 
                )
        )
    [message] => Successful!
)
```
