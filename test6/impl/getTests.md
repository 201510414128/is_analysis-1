<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getTests  [返回](../README.md)
用例： [修改实验](../用例/学生列表.md)

- 权限：
    访客/访客：无法修改
    老师：可以查看并修改实验。

- 功能：
    获取老师已发布的实验列表

- API请求地址：
   接口基本地址/v1/api/getTests

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
                {"TEST_ID": "201510414",
                "COURSE_ID": "20131",
                "TERM_ID": "1",
                "TEACHER_ID": "20141041",
                "TEST_TITLE": "实验二",
                "TEST_CONTENT": "本次实验..."},
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
  |total|返回发布的实验数量|
  |data|所有发布实验的数组|
  |TEST_ID|实验编号|
  |COURSE_ID|课程编号|
  |TERM_ID|学期编号|
  |TEACHER_ID|发布实验的教师工号|
  |TEST_TITLE|实验标题|
  |TEST_CONTENT|实验内容|
