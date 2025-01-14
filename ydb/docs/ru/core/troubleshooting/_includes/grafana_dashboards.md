## Сервис {{ ydb-full-name }} {#ydb}

### DB status {#dbstatus}

Общий дашборд базы данных.

### Actors {#actors}

Потребление CPU в актор-системе.

| **Имя** | **Описание** |
|---|---|
| CPU by execution pool (us) | Потребление CPU в различных пулах исполнения на всех нодах, микросекунды в секунду (один миллион соответствует потреблению одного ядра) |
| Actor count | Количество акторов (по типу актора) |
| CPU | Потребление CPU в различных пулах исполнения (по типу актора) |
| Events | Метрики обработки событий в актор-системе |

### gRPC {#grpc}

Метрики слоя gRPC.

| **Имя** | **Описание** |
|---|---|
| Requests | Количество запросов, получаемых базой данных в секунду (по типу метода gRPC) |
| Request bytes | Размер запросов, получаемых базой данных, байты в секунду (по типу метода gRPC) |
| Response bytes | Размер ответов, отправляемых базой данных, байты в секунду (по типу метода gRPC) |
| Dropped requests | Количество запросов в секунду, обработка которых была прекращена на транспортном уровне из-за ошибки (по типу метода gRPC) |
| Dropped responses | Количество ответов в секунду, отправка которых была прекращена на транспортном уровне из-за ошибки (по типу метода gRPC) |
| Requests in flight | Количество запросов, которые одновременно обрабатываются базой данных (по типу метода gRPC) |
| Request bytes in flight | Размер запросов, которые одновременно обрабатываются базой данных (по типу метода gRPC) |

### Query engine {#queryengine}

Сведения о движке исполнения запросов.

| **Имя** | **Описание** |
|---|---|
| Requests | Количество входящих запросов в секунду (по типу запроса) |
| Request bytes | Размер входящих запросов, байты в секунду (query, parameters, total) |
| Responses | Количество ответов в секунду (по типу ответа) |
| Response bytes | Размеры ответов, байты в секунду (total, query result) |
| Sessions | Сведения об установленных сессиях |
| Latencies | Гистограммы времён исполнения запросов для различных типов запросов |

### TxProxy {#txproxy}

Информация от транзакциях с уровня DataShard transaction proxy.

| **Имя** | **Описание** |
|---|---|
| Transactions | Метрики транзакций даташардов |
| Latencies | Гистограммы времён исполнения различных этапов транзакций даташардов |

### DataShard {#datashard}

Метрики таблетки DataShard.

| **Имя** | **Описание** |
|---|---|
| Operations | Статистика операций с даташардом для разных типов операций |
| Transactions | Информация о транзакциях таблетки даташарда (по типам транзакций) |
| Latencies | Гистограммы времён выполнения различных этапов пользовательских транзакций |
| Tablet latencies | Гистограммы времён выполнения транзакций таблетки |
| Compactions | Сведения о производимых операциях LSM compaction |
| ReadSets | Сведения о пересылаемых ReadSets при исполнении пользовательской транзакции |
| Other | Прочие метрики |

