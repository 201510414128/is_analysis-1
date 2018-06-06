<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getGradesStandard  [返回](../README.md)
用例： [评改成绩](../用例/学生列表.md)

- 权限：
    访客：无法获取评分标准列表
    学生：可以查看评分标准列表
    老师：可以查看和修改评分标准列表。

- 功能：
    返回评分标准列表。

- API请求地址：
   接口基本地址/v1/api/getGradesStandard

- 请求方式 ：
    POST

- 请求实例： 

      {
           "test_id":3
      }
      
- 请求参数说明:

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |test_id|需获取评分标准的实验|


- 返回实例：

      {
            "status": true,
            "info": null,
            "total": 11,
            "data": [
                {"GRADE_ID": "1",
                 "TEST_ID": "3",
                 "STANDARD": "实验条理清晰",
                 "WEIGHT": "30",
                 "GRADE": "90"},
                {
                ...其他评分标准项
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回评分标准数量|
  |data|所有评分标准的数组|
  |GRADE_ID|评分标准编号|
  |TEST_ID|实验编号|
  |STANDARD|评分标准内容|
  |WEIGHT|分数所占比重|
  |GRADE|所得分数|
