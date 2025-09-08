
---
title: HarmBlock 思路
---


```mermaid
graph TD
    A["新媒体文件生成 (消息通知)"] --> B["file scan 收到消息 根据URI查数据库"]
    B --> C{"是否 JPG 文件?"}
    C -- "是" --> E{"JPG 是否 NSFW?"}
    E -- "是" --> F["删除 JPG (流程结束)"]
    E -- "否" --> D["检查xmp"]
    D -- "否" --> G["保留 JPG (流程结束)"]
    D -- "是" --> H["提取对应 MP4 文件送检"]
    H --> I{"MP4 是否 NSFW?"}
    I -- "是" --> J["删除 JPG 和临时 MP4 文件"]
    I -- "否" --> K["保留 JPG 并删除临时 MP4 文件"]
```

```mermaid
gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to mermaid
        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2               :         des4, after des3, 5d
        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to mermaid                      :1d
```
 ```mermaid
erDiagram
          CUSTOMER }|..|{ DELIVERY-ADDRESS : has
          CUSTOMER ||--o{ ORDER : places
          CUSTOMER ||--o{ INVOICE : "liable for"
          DELIVERY-ADDRESS ||--o{ ORDER : receives
          INVOICE ||--|{ ORDER : covers
          ORDER ||--|{ ORDER-ITEM : includes
          PRODUCT-CATEGORY ||--|{ PRODUCT : contains
          PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```

```mermaid
 graph TB
    subgraph 从左到右
        direction LR
        声明图像类型1 --> 声明排列方向1 --> 声明图像内容1
    end
    subgraph 从右到左
        direction RL
        声明图像类型2 --> 声明排列方向2 --> 声明图像内容2
    end
    subgraph 上下分明
        direction LR
        subgraph 从上到下
        direction TB
        声明图像类型3 --> 声明排列方向3 --> 声明图像内容3
        end
        subgraph 从下到上
        direction BT
        声明图像类型4 --> 声明排列方向4 --> 声明图像内容4
        end
        从上到下 --> 从下到上
    end
    从左到右 --> 从右到左 --> 上下分明
```
