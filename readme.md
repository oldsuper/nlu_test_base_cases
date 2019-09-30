#简介
通过我在NIO（蔚来汽车）和KT（盟游）的工作中的思考和实践，对后台接口做了一套自动化业务测试框架。
最主要的目的是通过自动化回归的方式完成“回归”测试，提供一种自助式的日常测试服务。
由于自动化测试远期的矛盾在于维护成本和项目迭代，通过测试数据和代码分离、检查点抽取和分层做了一些必要的优化。
*虽然本人在NIO独立设计、开发实现了几乎相同业务测试框架(从2017年5月至2019年7月我离开，该框架的设计思路和核心代码几乎没有变更，每周例行release2~3次，其间在不同分支上开发自测和自动触发大约20次/天)，为避免著作权的麻烦，本项目代码完全重写。
#目录结构
root
  |--conf //环境默认配置
  |--case //测试用例位置，可通过修改conf变更
  |--log
  |--report
  |--src
      |--utils
      		 |--m_struct.py //业务类
      		 |--m_request.py
      		 |--m_assert.py
      		 |--m_config.py
      |--test_main.py //入口
#使用方法
nosetest 
##基本命令
##参数