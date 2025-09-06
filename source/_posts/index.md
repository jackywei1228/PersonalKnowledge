---
title: Hello World
---

```mermaid
sequenceDiagram
title: 序列图
participant NetWork Thread
participant Message Thread
participant AI Thread


NetWork Thread->Message Thread: 收到网络信息
Message Thread->Message Thread: Paser处理信息
Message Thread->AI Thread: 解析好的信息

```

重新开始!