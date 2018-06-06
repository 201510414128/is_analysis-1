<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getTeachers  [返回](../README.md)
用例： [选择课程](../用例/学生列表.md)

- 权限：
    访客：无法选课。
    学生：可以选课。
    老师：可以选课。

- 功能：
    返回所有老师所选课程。

- API请求地址：
   接口基本地址/v1/api/getTeachers

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
                {"TEACHER_ID": "201510414",
                "DEPARTMENT": "信工学院",
                "COURSE_SUM": "1.2,2.3",
                "COURSE_NUM": "5",},
                {
                ...其他老师
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回教师人数|
  |data|所有教师的数组|
  |TEACHER_ID|教师工号|
  |DEPARTMENT|教师所属部门|
  |COURSE_SUM|教师选课列表|
  |COURSE_NUM|规定所选课程数量|
