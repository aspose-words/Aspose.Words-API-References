---
title: "Aspose::Words::PageSetup::get_TextOrientation Methode"
linktitle: "get_TextOrientation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_TextOrientation-Methode. Ermöglicht das Festlegen von TextOrientation für die gesamte Seite. Der Standardwert ist Horizontal in C++."
type: docs
weight: 45000
url: /de/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Ermöglicht das Festlegen von [TextOrientation](./) für die gesamte Seite. Der Standardwert ist [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Beispiele



Zeigt, wie man die Textausrichtung einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Setzen Sie die Eigenschaft "TextOrientation" auf "TextOrientation.Upward", um den gesamten Text um 90 Grad zu drehen.
// nach rechts, sodass aller links‑nach‑rechts‑Text jetzt von oben nach unten verläuft.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## Siehe auch

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
