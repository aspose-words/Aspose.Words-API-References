---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML 方法"
linktitle: "get_WordOpenXML"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML 方法。获取一个字符串，表示 C++ 中 FlatOpc 格式下节点中包含的 XML。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


获取一个字符串，表示节点中在 [FlatOpc](../../../aspose.words/saveformat/) 格式下包含的 XML。

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## 示例



展示如何获取 FlatOpc 格式下节点中包含的 XML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## 另见

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
