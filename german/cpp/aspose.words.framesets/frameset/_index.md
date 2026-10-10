---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Framesets::Frameset class. Stellt eine Frames‑Seite oder einen einzelnen Frame auf einer Frames‑Seite dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Stellt eine Frames-Seite oder einen einzelnen Frame auf einer Frames-Seite dar. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Frameset : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Ruft die Sammlung von untergeordneten Frames und Frames‑Seiten ab. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Liest oder legt die URL der Webseite oder den Dateinamen des Dokuments fest, das in diesem Frame angezeigt werden soll. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Liest oder legt einen Wert fest, der angibt, ob die in der Eigenschaft [FrameDefaultUrl](./get_framedefaulturl/) angegebene Webseite oder der Dokumentdateiname eine externe Ressource ist, mit der der Frame verknüpft ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Setter für [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Setter für [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
