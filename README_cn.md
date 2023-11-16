# driver for Erlang

mongo的驱动没有维护了 所以在开源驱动的基础上做出了一些修改 原驱动地址：https://github.com/comtihon/mongodb-erlang

## 支持srv连接模式

If you want to connect to a replica set _ReplicaSetName_ use this format

To connect to mongo by srv record use this format

```erlang
Seed = {srv, ["hostname1:port1", "hostname2:port2"]}
```

## 支持mongo op_msg 协议

```erlang
{use_legacy_protocol, true}
```

use_legacy_protocol
* true ： 使用老版本协议
* false ： 使用op_msg协议