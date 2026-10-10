---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal 方法"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal 方法。获取表示节点中以 FlatOpc 格式包含的 XML 的字符串。与 WordOpenXML 属性不同，此方法在 C++ 中生成一个剥离了所有非内容相关部分的精简文档。"
type: docs
weight: 20500
url: /zh/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


获取表示节点中包含的 XML 的字符串，采用 [FlatOpc](../../../aspose.words/saveformat/) 格式。与 [WordOpenXML](../get_wordopenxml/) 属性不同，此方法生成一个精简的文档，排除任何非内容相关的部分。

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## 示例



展示如何在 FlatOpc 格式中获取节点内的最小 XML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## 另见

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
