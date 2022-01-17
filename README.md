## Data Construction
We herein describe (a) Annotation of 1,000 Compression Data and (b) 151k parallel training data.

### (a) Annotation of 1,000 Compression Data
We have submitted 1,000 annotation corpus to the paper submission website. Three example sentences along with two annotated compressions are shown below:
 - Sentence-1: 哈特尔 在 接受 美联社 采访 时 表示 ，如果 下雨 ，空气 中 放射性 颗粒 就 会 消失 ，但是 受 核污染 的 食品 就 不同 了 。
 - Annotated Compression-a: 哈特尔 表示 如果 下雨 ，空气 中 放射性 颗粒 会 消失 ，但是 核污染 食品 不同
 - Annotated Compression-b: 哈特尔 表示 下雨 空气 中 放射性 颗粒 会 消失
 
<br>

 - Sentence-2: 据 报道 ，对于 朝鲜 三份 官方 报章 在 其 元旦 联合 社论 中 呼吁 尽早 结束 朝鲜半岛 南北 双方 的 紧张 对峙 ，韩国 高层 官员 作出 了 慎重 评价 。
 - Annotated Compression-a: 对于 朝鲜 呼吁 尽早 结束 南北 对峙 韩国 高层 作出 了 慎重 评价 
 - Annotated Compression-b: 朝鲜 三份 报章 呼吁 尽早 结束 朝鲜半岛 双方 的 对峙

<br>

 - Sentence-3: 稍早 ， 尼日尔 外长 证实 ，载有 利比亚 高级 逃犯 的 3 支 车队 抵达 尼日尔 。
 - Annotated Compression-a: 尼日尔 外长 证实 载有 逃犯 的 车队 抵达 尼日尔
 - Annotated Compression-b: 尼日尔 外长 证实 载有 逃犯 的 车队 抵达 尼日尔


### (b) 151k parallel training data
Once you download [Chinese Gigawords Third version](https://catalog.ldc.upenn.edu/LDC2007T38), you can reproduce the 151k pairs of sentence and compression following our [data construction procedure](https://github.com/ExperimentCode/code/blob/main/README.md#code-for-constructing-151k-data). Alternatively, you may download the [model](https://github.com/ExperimentCode/model) we trained using 151k pairs of sentence and compression without accessing the Chinese Gigawords corpus. 
