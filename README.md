## 前言

欢迎来到基于Spring Boot的高校请假管理系统项目。本系统旨在为高校提供一个高效、便捷的请假管理平台，使教师和学生能够轻松地处理请假事宜，提高学校管理效率。

## 内容介绍

本系统主要包括以下几个模块：

1. **请假申请**：学生可在线提交请假申请，包括请假原因、开始时间、结束时间等信息。
2. **请假审批**：教师可查看学生的请假申请，并进行审批或驳回操作。
3. **请假记录**：学生和教师可以查看历史请假记录，了解请假情况。
4. **个人中心**：学生和教师可查看和修改个人信息，如姓名、性别、联系电话等。

系统采用前后端分离的架构，前端使用Vue框架实现，后端则基于Spring Boot框架。数据库采用MySQL进行数据存储。

## 技术介绍

- **语言**：Java
- **使用框架**：Spring Boot
- **前端技术**：JS、Vue、CSS3
- **开发工具**：IDEA/Eclipse
- **数据库**：MySQL 5.7/8.0
- **数据库管理工具**：phpstudy/Navicat
- **JDK版本**：jdk1.8
- **Maven**：apache-maven 3.8.1-bin
- **前端环境**：Node.js 12/14/16

## 核心代码

```java
// 请假申请Controller
@RestController
@RequestMapping("/leave")
public class LeaveController {

    @Autowired
    private LeaveService leaveService;

    // 提交请假申请
    @PostMapping("/apply")
    public Response applyLeave(@RequestBody LeaveApply leaveApply) {
        boolean result = leaveService.applyLeave(leaveApply);
        return new Response(result ? Code.SUCCESS : Code.FAIL);
    }

    // 查看请假记录
    @GetMapping("/record")
    public Response getLeaveRecord(@RequestParam("studentId") String studentId) {
        List<LeaveRecord> recordList = leaveService.getLeaveRecord(studentId);
        return new Response(recordList);
    }

    // 教师审批请假申请
    @PutMapping("/approve")
    public Response approveLeave(@RequestParam("leaveId") String leaveId, @RequestParam("status") int status) {
        boolean result = leaveService.approveLeave(leaveId, status);
        return new Response(result ? Code.SUCCESS : Code.FAIL);
    }
}
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

# 项目截图

![封面图片](https://img10.360buyimg.com/ddimg/jfs/t1/333486/15/10277/95163/68bc7233F6cc6ce1e/174cc9a048ac79cc.jpg)

![介绍图片](https://img11.360buyimg.com/ddimg/jfs/t1/349398/8/458/30722/68bc7218F209aedc3/bf764e2721819b64.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/340247/22/7840/31012/68bc7219Fd513407b/3d655196416a3f0b.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/342846/21/337/17442/68bc7219F59c344a6/af2e036ed6aa56c0.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/347261/18/490/18637/68bc721aFe30b1117/c04d0f81ad78a88c.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/332518/27/10242/14028/68bc721aF8e34dba6/2061a95a4ffbc3c3.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/350276/21/474/29548/68bc721bF017441e5/1e98f01656d4199f.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/347280/8/429/26325/68bc721bFdbc42f16/f688b47051c30273.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/327897/26/16979/27002/68bc721bFb89dd473/256d2bb0cf06119c.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/330640/1/10450/19184/68bc721cFb9caa889/a24f7729b0edaf73.jpg)


## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
