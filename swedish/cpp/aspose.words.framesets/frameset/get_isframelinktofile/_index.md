---
title: "Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile metod"
linktitle: "get_IsFrameLinkToFile"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile metod. Hämtar eller anger ett värde som indikerar om webbsidan eller dokumentfilnamnet som anges i egenskapen FrameDefaultUrl är en extern resurs som ramen är länkad till i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.framesets/frameset/get_isframelinktofile/
---
## Frameset::get_IsFrameLinkToFile method


Hämtar eller anger ett värde som indikerar om webbsidan eller dokumentfilnamnet som anges i egenskapen [FrameDefaultUrl](../get_framedefaulturl/) är en extern resurs som ramen är länkad till.

```cpp
bool Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile()
```


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

* Class [Frameset](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
