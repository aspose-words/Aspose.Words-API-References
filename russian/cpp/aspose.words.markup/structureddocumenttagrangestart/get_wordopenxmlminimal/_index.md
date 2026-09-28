---
title: "Метод Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal. Возвращает строку, представляющую XML, содержащийся в узле в формате FlatOpc. В отличие от свойства WordOpenXML, этот метод генерирует упрощённый документ, исключающий любые части, не связанные с содержимым, в C++."
type: docs
weight: 20500
url: /ru/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Возвращает строку, представляющую XML, содержащийся в узле в формате [FlatOpc](../../../aspose.words/saveformat/). В отличие от свойства [WordOpenXML](../get_wordopenxml/), этот метод генерирует упрощённый документ, исключающий любые части, не связанные с содержимым.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Примеры



Показывает, как получить минимальный XML, содержащийся в узле, в формате FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## См. также

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
