# 基于GitHub的实验管理平台的分析与设计

### 成都大学信息科学与工程学院

|学号|班级|姓名|
|:-------:|:-------------: | :----------:|
|201510414113|软件(本)15-1|江自杰|

## 1. 概述
- 基于GitHub的实验管理平台的作用是在线管理实验成绩的Web应用系统。学生和老师的实验内容均存放在GitHUB
页面上。
- 学生的功能主要有：一是设置自己的GitHub用户名，二是查询自己某学期，某课程的实验成绩。学生的GitHub用户名是公开的，但成绩不公开。
- 老师的功能主要有：一是批改某学期，某课程下每个学生的成绩，二是查看该学生的各个实验成绩。
- 老师和学生都能通过本系统的链接方便地跳转到学生的每个GitHUB实验目录，以便批改实验或者查看实验情况。
- 实验成绩按数字分数计算，每项实验的满分为100分，最低为0分。
- 系统自动计算每个学生的所有实验的平均分。
    
## 2. 系统总体结构
![](系统总体结构.png)

界面设计参见：https://jiangzijie123.github.io/is_analysis/test6/ui3/index.html

## 3. 用例图设计 [源码](src/UseCase.puml)
![](UseCase.png)

## 4. 类图设计 [源码](src/class.puml)
![](class.png)

## 5. 数据库设计
- ### [参见数据库设计](数据库设计.md)

## 6. 用例及界面详细设计
- ### [“学生列表”用例](./usecase/学生列表.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/index.html)
- ### [“评改成绩”用例](./usecase/评改成绩.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/评定成绩.html)
- ### [“查看成绩”用例](./usecase/查看成绩.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/查看成绩.html)
- ### [“选择课程”用例](./usecase/选择课程.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/选课.html)
- ### [“发布实验”用例](./usecase/发布实验.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/发布实验.html)
- ### [“修改实验”用例](./usecase/修改实验.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/修改实验.html)
- ### [“修改用户信息”用例](./usecase/修改用户信息.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/修改用户信息.html)
- ### [“查看用户信息”用例](./usecase/查看用户信息.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/查看用户信息.html)
- ### [“登出”用例](./usecase/登出.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/登出.html)
- ### [“登录”用例](./usecase/登录.md),[界面](https://jiangzijie123.github.io/is_analysis/test6/ui3/登录.html)
