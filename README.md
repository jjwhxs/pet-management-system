### 系统介绍

基于SpringBoot 和 Vue 实现的宠物管理系统采用前后端分离的架构方式，实 现了系统登录、首页、会员管理、会员充值、宠物类型、宠物档案、疫苗记 录、医疗记录、宠物用品、订单管理、索赔记录、管理员管理等功能模块。

### 技术选型

开发工具：idea2022.3+webstorm2021.1

运行环境：jdk1.8+maven3.6.3+mysql8.0+nodejs14.21.3

服务端技术：springboot+mybatis-plus+jwt+fastjson

前端技术：html+css+vue+axios+element-ui+echarts

### 成果展示

系统登录
<img width="1899" height="1025" alt="登录" src="https://github.com/user-attachments/assets/ff07aaf5-4b02-4900-802f-5a9638fdb696" />

首页
<img width="1900" height="1025" alt="首页" src="https://github.com/user-attachments/assets/938fa0c1-8886-4d6c-bc0a-67679018356c" />

会员管理
<img width="1899" height="1025" alt="会员管理" src="https://github.com/user-attachments/assets/c42ab797-3564-43d2-96da-90675b68a6af" />

会员充值
<img width="1903" height="1025" alt="会员充值" src="https://github.com/user-attachments/assets/9012ce5f-753e-4ede-8644-47bf13adb074" />

宠物类型
<img width="1905" height="1025" alt="宠物类型" src="https://github.com/user-attachments/assets/a65d9507-21d8-442f-a9c3-24b18bece4f4" />

宠物档案
<img width="1900" height="1024" alt="宠物档案" src="https://github.com/user-attachments/assets/cca18a49-7397-43a9-9390-1b3c5a727b15" />

疫苗记录
<img width="1904" height="1025" alt="疫苗记录" src="https://github.com/user-attachments/assets/dd9ec7ad-0fb5-4633-bc85-17a316e5f6bf" />

医疗记录
<img width="1900" height="1025" alt="医疗记录" src="https://github.com/user-attachments/assets/8c2d92c2-94fb-461b-b658-062d3ccc4133" />

宠物用品
<img width="1900" height="1020" alt="宠物用品" src="https://github.com/user-attachments/assets/7ef8ab94-64b1-43a4-80cf-e6d0871a1633" />

订单管理
<img width="1899" height="1025" alt="订单管理" src="https://github.com/user-attachments/assets/d291eebd-279b-4471-b827-df14993faa42" />

索赔记录
<img width="1906" height="1021" alt="索赔记录" src="https://github.com/user-attachments/assets/aa1be56f-974a-45df-bdf9-9d67eb24c616" />

### 源码展示

@RestController

@RequestMapping("/petType")

public class PetTypeController extends BaseController {

@Autowired

private IPetTypeService iPetTypeService;

//获取宠物类型列表

@GetMapping("/pageList")

public R pageList(PetTypeRequest request) {

    return iPetTypeService.pageList(request);
    
}

//添加宠物类型

@PostMapping("/add")

public R add(@RequestBody PetType petType) {

    return iPetTypeService.add(petType);
    
}

//更新宠物类型

@PutMapping("/update")

public R update(@RequestBody PetType petType) {

    return iPetTypeService.update(petType);
    
}

//删除宠物类型

@DeleteMapping("/delete")

public R delete(@RequestParam Integer id) {

    return iPetTypeService.delete(id);
    
}

//获取宠物类型详情

@GetMapping("/detail")

public R detail(@RequestParam Integer id) {

    return iPetTypeService.detail(id);
    
}

}

### 账号地址及其它说明

1、地址说明

登录页：localhost:8080

2、账号说明

管理员：admin/admin

3、目录结构展示

<img width="593" height="175" alt="目录结构" src="https://github.com/user-attachments/assets/efe98a89-e1e2-4316-9ce4-20e01d3a53b0" />

4、项目结构展示

<img width="1500" height="584" alt="项目结构" src="https://github.com/user-attachments/assets/59a2d750-6043-4a75-98c4-809e92dc17bb" />

5、运行步骤

1）创建数据库、导入sql脚本

2）修改application.properties中的数据库配置文件，启动服务端

3）在前端工程根目录下打开cmd，执行npm install下载依赖

4）下载完毕后启动前端npm run serve，访问端口

获取方式(可远程调试)
访问链接(在浏览器中手动输入下图中的地址)：

<img width="1124" height="136" alt="链接" src="https://github.com/user-attachments/assets/2ca8063e-7114-4cae-8e22-9a35b26a2502" />

若资源获取失败，可添加happy35596339(vx)或2061772307(qq)进行交流
