---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_RangeEnd method
linktitle: get_RangeEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_RangeEnd method. Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. Otherwise returns null in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_rangeend/
---
## StructuredDocumentTagRangeStart::get_RangeEnd method


Specifies end of range if the [StructuredDocumentTag](../../structureddocumenttag/) is a ranged structured document tag. Otherwise returns **null**.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagRangeEnd> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_RangeEnd()
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

* Class [StructuredDocumentTagRangeEnd](../../structureddocumenttagrangeend/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
