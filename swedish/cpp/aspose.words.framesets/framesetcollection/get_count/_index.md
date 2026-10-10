---
title: "Aspose::Words::Framesets::FramesetCollection::get_Count metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Framesets::FramesetCollection::get_Count metod. Hämtar antalet ramar eller ram‑sidor som finns i samlingen i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.framesets/framesetcollection/get_count/
---
## FramesetCollection::get_Count method


Hämtar antalet ramar eller ram-sidor som finns i samlingen.

```cpp
int32_t Aspose::Words::Framesets::FramesetCollection::get_Count()
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

* Class [FramesetCollection](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
