---
title: Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML method
linktitle: get_WordOpenXML
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML method. Gets a string that represents the XML contained within the node in the FlatOpc format in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.markup/structureddocumenttag/get_wordopenxml/
---
## StructuredDocumentTag::get_WordOpenXML method


Gets a string that represents the XML contained within the node in the [FlatOpc](../../../aspose.words/saveformat/) format.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXML() override
```


## Examples



Shows how to get XML contained within the node in the FlatOpc format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
