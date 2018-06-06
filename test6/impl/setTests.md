<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setTests  [返回](../README.md)
用例： [发布实验](../用例/登出.md)

- 功能：
    添加发布的实验。
    
- 权限：
    学生已经登录。    
    
- API请求地址： 
    接口基本地址/v1/api/setTests

- 请求方式 ：
    POST

- 请求实例：

        {
            "test_id":1,
            "term_id":2,
            "course_id":3,
            "teacher_id":"4",
            "test_title":实验二,
            "test_content":此次实验是...
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |test_id|实验编号|
  |term_id|学期编号|
  |course_id|课程编号|
  |teacher_id|教师编号|
  |test_title|实验标题|
  |test_content|实验内容|
  
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


