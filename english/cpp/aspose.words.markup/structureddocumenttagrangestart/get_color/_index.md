---
title: get_Color
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the color of the structured document tag.
type: docs
weight: 53
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_color/
---
## StructuredDocumentTagRangeStart.get_Color method


Gets or sets the color of the structured document tag.

```cpp
System::Drawing::Color Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color() override
```


## Examples




Shows how to get the properties of multi-section structured document tags. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Multi-section structured document tags.docx");

auto rangeStartTag =
    System::DynamicCast_noexcept<StructuredDocumentTagRangeStart>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag =
    System::DynamicCast_noexcept<StructuredDocumentTagRangeEnd>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

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

