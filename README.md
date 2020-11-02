DataX数据同步框架的clickhousereader插件
1.clickhouse reader插件支持的功能：基于datax同步框架，使用插件流式读取clickhouse。
2.经过测试的数据源有 MySQL，ElasticSearch，Hive，Clickhouse。
3.Job参数优化：
"setting": {
      "speed": {
        "channel": 6,#选择合适的通道数
        "byte": 10485760 #根据实际资源控制每个通到的容量
      }
    }
 4.根据实际同步的数据量与集群资源配置适当的内存参数
 -Xms4096m -Xmx4096m -XX:+HeapDumpOnOutOfMemoryError
