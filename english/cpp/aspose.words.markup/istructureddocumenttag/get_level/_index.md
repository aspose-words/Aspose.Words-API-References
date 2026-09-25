---
title: Aspose::Words::Markup::IStructuredDocumentTag::get_Level method
linktitle: get_Level
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::get_Level method. Gets the level at which this SDT occurs in the document tree in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.markup/istructureddocumenttag/get_level/
---
## IStructuredDocumentTag::get_Level method


Gets the level at which this **SDT** occurs in the document tree.

```cpp
virtual Aspose::Words::Markup::MarkupLevel Aspose::Words::Markup::IStructuredDocumentTag::get_Level() const =0
```


## Examples



Shows how to get the properties of multi-section structured document tags. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Multi-section structured document tags.docx"));

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

System::Console::WriteLine(u"StructuredDocumentTagRangeStart values:");
System::Console::WriteLine(System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()));
System::Console::WriteLine(System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()));
System::Console::WriteLine(System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()));
System::Console::WriteLine(System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()));
System::Console::WriteLine(System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()));
System::Console::WriteLine(System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()));
System::Console::WriteLine(System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()));
System::Console::WriteLine(System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()));
System::Console::WriteLine(System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()));
System::Console::WriteLine(System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()));
System::Console::WriteLine(System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()));
System::Console::WriteLine(System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()));
System::Console::WriteLine(System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()));

System::Console::WriteLine(u"StructuredDocumentTagRangeEnd values:");
System::Console::WriteLine(System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()));
System::Console::WriteLine(System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()));
```

## See Also

* Enum [MarkupLevel](../../markuplevel/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
