---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML 方法"
linktitle: "get_WordOpenXML"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML 方法。获取表示节点中以 FlatOpc 格式包含的 XML 的字符串（在 C++ 中）。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxml/
---
## StructuredDocumentTag::get_WordOpenXML method


获取一个字符串，表示节点中在 [FlatOpc](../../../aspose.words/saveformat/) 格式下包含的 XML。

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML() override
```


## 示例



展示如何获取 FlatOpc 格式下节点中包含的 XML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## 另见

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
