---
title: "Aspose::Words::Document::get_Frameset-Methode"
linktitle: "get_Frameset"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_Frameset-Methode. Gibt eine Frameset-Instanz zurück, wenn dieses Dokument eine Frames-Seite in C++ darstellt."
type: docs
weight: 27000
url: /de/cpp/aspose.words/document/get_frameset/
---
## Document::get_Frameset method


Gibt eine [Frameset](./)-Instanz zurück, wenn dieses Dokument eine Frames-Seite darstellt.

```cpp
System::SharedPtr<Aspose::Words::Framesets::Frameset> Aspose::Words::Document::get_Frameset() const
```


## Beispiele



Zeigt, wie man Frames auf der Seite zugreift.
```cpp
// Das Dokument enthält mehrere Frames mit Links zu anderen Dokumenten.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Wir können die Standard‑URL (eine Webseiten‑URL oder ein lokales Dokument) prüfen oder ob der Frame eine externe Ressource ist.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Ändern Sie die Eigenschaften eines unserer Frames.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## Siehe auch

* Class [Frameset](../../../aspose.words.framesets/frameset/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
