---
title: "Aspose::Words::Fields::FieldStart::Accept 方法"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldStart::Accept 方法。接受在 C++ 中的访问者。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


接受访问者。

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问该节点的访问者。 |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## 备注


调用 [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/)。

更多信息请参阅 Visitor 设计模式。

## 另见

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
