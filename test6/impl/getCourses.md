<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getCourses  [返回](../README.md)
用例： [选择课程](../用例/学生列表.md)

- 权限：
    访客：不能进行选课
    学生：可以进行选课，但只能在老师之后选。
    老师：可以进行选课。

- 功能：
    返回可选的课程列表。

- API请求地址：
   接口基本地址/v1/api/getCourses

- 请求方式 ：
    GET

- 请求参数说明:
    无

- 返回实例：

      {
            "status": true,
            "info": null,
            "total": 121,
            "data": [
                {"COURSE_ID": "2013123",
                "TERM_ID": "1",
                "COURSE_NAME": "信息系统分析与设计",
                "COURSE_DETAIL": "本课程...",
                "STU_NUM": "120",
                "TEA_NUM": "2",
                "STU_TIME_START": "2018-04-02 13:48:01"
                "STU_TIME_END": "2018-04-02 13:48:01"
                "TEA_TIME_START": "2018-04-02 13:48:01"
                "TEA_TIME_END": "2018-04-02 13:48:01"},
                {
                ...其他实验
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回课程数量|
  |data|所有课程的数组|
  |COURSE_ID|课程编号|
  |TERM_ID|学期编号|
  |COURSE_NAME|课程名称|
  |COURSE_DETAIL|课程详情|
  |STU_NUM|最大学生人数|
  |TEA_NUM|最大老师人数|
  |STU_TIME_START|学生选课开始日期|
  |STU_TIME_END|学生选课结束日期|
  |TEA_TIME_START|老师选课开始日期|
  |TEA_TIME_END|老师选课结束日期|
