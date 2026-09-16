---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart method"
linktitle: "VisitFieldStart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart method. 当文档中的字段开始时调用，此方法适用于 C++。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


当文档中的字段开始时调用。

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | 正在被访问的对象。 |

### ReturnValue

一个指定如何继续枚举的 [VisitorAction](../../visitoraction/) 值。
## 备注


Word 文档中的字段由字段代码和字段值组成。

例如，显示页码的字段可以表示如下：

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

字段分隔符将文档中的字段代码与字段值分开。请注意，某些字段只有字段代码，没有字段分隔符和字段值。

[Fields](../../../aspose.words.fields/) can be nested.

## 另见

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
