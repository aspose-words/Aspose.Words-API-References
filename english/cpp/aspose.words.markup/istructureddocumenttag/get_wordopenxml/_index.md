---
title: Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML method
linktitle: get_WordOpenXML
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML method. Gets a string that represents the XML contained within the node in the FlatOpc format in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


Gets a string that represents the XML contained within the node in the [FlatOpc](../../../aspose.words/saveformat/) format.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## Examples



Shows how to get XML contained within the node in the FlatOpc format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## See Also

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
