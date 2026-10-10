---
title: "Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile Methode"
linktitle: "get_IsFrameLinkToFile"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile Methode. Ruft einen Wert ab oder legt ihn fest, der angibt, ob die in der FrameDefaultUrl‑Eigenschaft angegebene Webseite oder der Dateiname des Dokuments eine externe Ressource ist, mit der das Frame verknüpft ist, in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.framesets/frameset/get_isframelinktofile/
---
## Frameset::get_IsFrameLinkToFile method


Ruft einen Wert ab oder legt ihn fest, der angibt, ob die in der [FrameDefaultUrl](../get_framedefaulturl/)‑Eigenschaft angegebene Webseite oder der Dateiname des Dokuments eine externe Ressource ist, mit der das Frame verknüpft ist.

```cpp
bool Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile()
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

* Class [Frameset](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
