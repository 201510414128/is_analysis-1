﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getGrades  [返回](../README.md)
用例： [查看成绩](../usecase/查看成绩.md)

- 权限：
    访客：无法查看成绩
    学生：可以查看自己所有实验成绩
    老师：只能查看自己所授课程中学生的成绩。

- 功能：
    返回成绩列表。

- API请求地址：
   接口基本地址/v1/api/getGrades

- 请求方式 ：
    POST
- 请求实例： 

      {
           "student_id":20130103
      }
      
- 请求参数说明:

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |student_id|需获取实验成绩的学生学号|

- 返回实例：

      {
            "status": true,
            "info": null,
            "total": 11,
            "data": [
                {"STUDENT_ID": "20130103",
                "TEST_ID": "201301",
                 "GRADE_SUM": "1，2，3",
                 "MEMO": "该生此次实验...",
                 "UPDATE_DATE": "2018-06-03 12:23:93"},
                {
                ...其他课程
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回实验成绩数量|
  |data|所有实验成绩的数组|
  |STUDENT_ID|学生学号|
  |TEST_ID|实验编号|
  |GRADE_SUM|评分标准项的汇总|
  |MEMO|实验评语|
  |UPDATE_DATE|实验评改日期|
