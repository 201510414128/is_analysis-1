<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setTeachers  [返回](../README.md)
用例： [选择课程](../usecase/选择课程.md)

- 功能：
    设置老师的选课列表。
    
- 权限：
    老师已经登录并选课。    
    
- API请求地址： 
    接口基本地址/v1/api/setTeachers

- 请求方式 ：
    POST

- 请求实例：

        {
            "teacher_id":324111,
            "course_sum":"1.2,2.3",
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |teacher_id|教师工号|
  |course_sum|学生选课列表汇总|
  
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


