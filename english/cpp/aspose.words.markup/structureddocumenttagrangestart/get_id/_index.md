---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Id method
linktitle: get_Id
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Id method. Specifies a unique read-only persistent numerical Id for this structured document tag in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_id/
---
## StructuredDocumentTagRangeStart::get_Id method


Specifies a unique read-only persistent numerical Id for this structured document tag.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Id() override
```

## Remarks


Id attribute shall follow these rules:* The document shall retain structured document tag ids only if the whole document is cloned [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other structured document tag Ids in the target document.
* If multiple structured document tag nodes specify the same decimal number value for the Id attribute, then the first structured document tag in the document shall maintain this original Id, and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone structured document tag [Clone()](../) operation new unique ID will be generated for the cloned structured document tag node.
* If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned to it when the document is loaded.



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

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
