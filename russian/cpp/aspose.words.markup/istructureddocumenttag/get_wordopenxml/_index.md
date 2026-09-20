---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML метод"
linktitle: "get_WordOpenXML"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML. Возвращает строку, представляющую XML, содержащийся в узле в формате FlatOpc в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


Возвращает строку, представляющую XML, содержащийся в узле в формате [FlatOpc](../../../aspose.words/saveformat/).

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## Примеры



Показано, как получить XML, содержащийся в узле в формате FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## См. также

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
