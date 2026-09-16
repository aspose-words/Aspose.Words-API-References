---
title: "Aspose::Words::Document::Accept 方法"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::Accept 方法。接受一个访问者（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/document/accept/
---
## Document::Accept method


接受访问者。

```cpp
bool Aspose::Words::Document::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问这些节点的访问者。 |

### ReturnValue

如果所有节点都已访问则为 true；如果在访问所有节点之前 [DocumentVisitor](../../documentvisitor/) 停止了操作则为 false。
## 备注


遍历此节点及其所有子节点。每个节点都会调用 [DocumentVisitor](../../documentvisitor/) 上的相应方法。

更多信息请参阅 Visitor 设计模式。

## 另见

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
