<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setGrades  [返回](../README.md)
用例： [评改成绩](../usecase/评改成绩.md)

- 功能：
    老师评改学生实验成绩。
    
- 权限：
    老师已经登录。    
    
- API请求地址： 
    接口基本地址/v1/api/setGrades

- 请求方式 ：
    POST

- 请求实例：

        {
            "student_id":324111,
            "test_id":324111,
            "grade_sum":1,2,3,
            "memo":此次实验...,
            "update_date":2018-06-06 12:00:00
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学生学号|
  |test_id|实验编号|
  |grade_sum|评分标准汇总|
  |memo|实验评语|
  |update_date|实验评改日期|
  
- 返回实例：

        {         
            "status": true,
            "info": null,    

        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


