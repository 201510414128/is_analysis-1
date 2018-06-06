<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setGradesStandard [返回](../README.md)
用例： [评改成绩](../用例/登出.md)

- 功能：
    老师评改学生实验成绩进行打分。
    
- 权限：
    老师已经登录。    
    
- API请求地址： 
    接口基本地址/v1/api/setGradesStandard

- 请求方式 ：
    POST

- 请求实例：

        {
            "grade_id":324111,
            "test_id":324111,
            "grade":1,2,3,
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |grade_id|评分标准编号|
  |test_id|实验编号|
  |grade|分数|
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


