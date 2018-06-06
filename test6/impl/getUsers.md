<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getUsers  [返回](../README.md)
用例： [修改用户信息](../用例/学生列表.md)

- 权限：
    访客：无法修改。
    老师/学生：可以查看并修改用户信息。

- 功能：
    获取用户信息

- API请求地址：
   接口基本地址/v1/api/getUsers

- 请求方式 ：
    GET

- 请求参数说明:
    无

- 返回实例：

        {
            "status": true,
            "info": null,
            "total": 20,
            "data": [
                {"USER_ID": "201510414",
                "NAME": "江自杰",
                "GITHUB_USERNAME": "jiang",
                "UPDATE_DATE": "2014-10-04 11:23:22",
                "PASSWORD": "123456",
                "DISABLE": "否"},
                {
                ...其他已发布的实验
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回用户信息数量|
  |data|所有用户信息的数组|
  |USER_ID|用户编号|
  |NAME|用户真实名称|
  |GITHUB_USERNAME|GITHUB账号名|
  |UPDATE_DATE|GITHUB账号修改日期|
  |PASSWORD|密码|
  |DISABLE|用户是否可用|
