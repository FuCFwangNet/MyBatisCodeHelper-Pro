## 快速测试mybatis的sql

当我们写完sql后，我们需要测试下sql是否符合预期，在填入各种参数后能否正常工作，尤其是对于复杂的sql。

一般我们测试可能是如下的代码:

![springTestCase](https://gejun123456.coding.net/p/MyBatisCodeHelper-Pro/d/MyBatisCodeHelper-Pro/git/raw/master/screenshots/springtestCase.gif)

由于需要启动spring，当项目较大的时候启动速度很慢，有些项目的启动时间超过30秒。导致测试sql速度很慢，改下sql重新再测试等很花时间。


如果只是单独测试sql是否正确，没必要启动spring容器，mybatis可以直接定义配置文件进行启动,如下

![quickTestJavaMapper](https://gejun123456.coding.net/p/MyBatisCodeHelper-Pro/d/MyBatisCodeHelper-Pro/git/raw/master/screenshots/quickTestJavaMapper.png)

配置文件
![quickTestConfiguration](https://gejun123456.coding.net/p/MyBatisCodeHelper-Pro/d/MyBatisCodeHelper-Pro/git/raw/master/screenshots/quickTestConfiguration.png)

这样我们可以直接测试mybatis的sql而不需要启动spring

速度非常快 如下：

![testSpeed](https://gejun123456.coding.net/p/MyBatisCodeHelper-Pro/d/MyBatisCodeHelper-Pro/git/raw/master/screenshots/quickTestNoSpring.gif)

基本上1，2秒钟就跑完了。 相比启动spring的测试效率提升很高。

插件可以自动生成测试的java类和配置文件，不需要手动去配置。

![generateTestcase](https://gejun123456.coding.net/p/MyBatisCodeHelper-Pro/d/MyBatisCodeHelper-Pro/git/raw/master/screenshots/autoGenerateTestCase.gif)


另外插件还可以快速构造测试数据，从表里面的数据生成java构造bean语句，提升写测试的效率

![GenerateJavaSetterFromTableRow](https://gejun123456.coding.net/p/MyBatisCodeHelper-Pro/d/MyBatisCodeHelper-Pro/git/raw/master/screenshots/GenerateJavaSetterFromTableRow.gif)










