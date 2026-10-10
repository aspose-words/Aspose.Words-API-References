---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator 方法"
linktitle: "VisitFieldSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator 方法。当在 C++ 文档中遇到字段分隔符时调用。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


当文档中遇到字段分隔符时调用。

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | 正在被访问的对象。 |

### ReturnValue

一个指定如何继续枚举的 [VisitorAction](../../visitoraction/) 值。
## 备注


字段分隔符将文档中的字段代码与字段值分开。请注意，某些字段只有字段代码，没有字段分隔符和字段值。

更多信息请参见 [VisitFieldStart()](../visitfieldstart/)

## 另见

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
