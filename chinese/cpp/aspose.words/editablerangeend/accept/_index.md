---
title: "Aspose::Words::EditableRangeEnd::Accept 方法"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EditableRangeEnd::Accept 方法。C++ 中接受访问者。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


接受访问者。

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问该节点的访问者。 |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## 备注


调用 [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/)。

更多信息请参阅 Visitor 设计模式。

## 另见

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
