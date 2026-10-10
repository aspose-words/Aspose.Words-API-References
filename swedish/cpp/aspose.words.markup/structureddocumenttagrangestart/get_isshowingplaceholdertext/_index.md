---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText metod"
linktitle: "get_IsShowingPlaceholderText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText metod. Anger huruvida innehållet i detta strukturerade dokumenttagg ska tolkas som platshållartext (i motsats till vanlig text). Om satt till true ska detta tillstånd återupptas (visa platshållartext) vid öppning av dokumentet i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.markup/structureddocumenttagrangestart/get_isshowingplaceholdertext/
---
## StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText method


Anger om innehållet i detta strukturerade dokumenttagg ska tolkas som platshållartext (i motsats till vanligt textinnehåll inom det strukturerade dokumenttagget). Om det är satt till **true** återupptas detta tillstånd (visar platshållartext) när dokumentet öppnas.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText() override
```


## Exempel



Visar hur man får egenskaperna för strukturerade dokumenttaggar med flera sektioner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Se även

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
