---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Framesets::Frameset-klass. Representerar en ram-sida eller en enskild ram på en ram-sida. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Representerar en frames-sida eller en enskild ram på en frames-sida. För att lära dig mer, besök [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokumentationsartikel.

```cpp
class Frameset : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Hämtar samlingen av underramar och ram-sidor. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Hämtar eller anger webbsidans URL eller dokumentfilens namn som ska visas i denna ram. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Hämtar eller anger ett värde som indikerar om webbsidan eller dokumentfilens namn som specificerats i egenskapen [FrameDefaultUrl](./get_framedefaulturl/) är en extern resurs som ramen är länkad till. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Sättare för [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Sättare för [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man får åtkomst till ramar på sidan.
```cpp
// Dokumentet innehåller flera ramar med länkar till andra dokument.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Vi kan kontrollera standard-URL:en (en webbsida-URL eller ett lokalt dokument) eller om ramen är en extern resurs.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Ändra egenskaper för en av våra ramar.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## Se även

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
