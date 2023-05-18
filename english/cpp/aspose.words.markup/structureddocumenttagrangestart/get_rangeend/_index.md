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
auto doc = MakeObject<Document>(MyDir + u"Multi-section structured document tags.docx");

auto rangeStartTag =
    System::AsCast<StructuredDocumentTagRangeStart>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag =
    System::AsCast<StructuredDocumentTagRangeEnd>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << "\t|Id: " << rangeStartTag->get_Id() << std::endl;
std::cout << "\t|Title: " << rangeStartTag->get_Title() << std::endl;
std::cout << "\t|PlaceholderName: " << rangeStartTag->get_PlaceholderName() << std::endl;
std::cout << String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << "\t|RangeEnd: " << rangeStartTag->get_RangeEnd() << std::endl;
std::cout << "\t|Color: " << rangeStartTag->get_Color().ToArgb() << std::endl;
std::cout << String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << "\t|Tag: " << rangeStartTag->get_Tag() << "\n" << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << "\t|Id: " << rangeEndTag->get_Id() << std::endl;
std::cout << String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## See Also

* Class [StructuredDocumentTagRangeEnd](../../structureddocumenttagrangeend/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
