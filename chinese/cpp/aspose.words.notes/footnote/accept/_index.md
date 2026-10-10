---
title: "Aspose::Words::Notes::Footnote::Accept 方法"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::Footnote::Accept 方法。接受访问者（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.notes/footnote/accept/
---
## Footnote::Accept method


接受访问者。

```cpp
bool Aspose::Words::Notes::Footnote::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问这些节点的访问者。 |

### ReturnValue

如果所有节点都已被访问则为 True；如果 [DocumentVisitor](../../../aspose.words/documentvisitor/) 在访问所有节点之前停止了操作则为 false。
## 备注


遍历此节点及其所有子节点。每个节点都会调用 [DocumentVisitor](../../../aspose.words/documentvisitor/) 上的相应方法。

更多信息请参阅 Visitor 设计模式。

## 另见

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
