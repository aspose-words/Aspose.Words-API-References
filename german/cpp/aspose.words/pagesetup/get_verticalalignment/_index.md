---
title: "Aspose::Words::PageSetup::get_VerticalAlignment-Methode"
linktitle: "get_VerticalAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_VerticalAlignment-Methode. Gibt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt zurück oder legt sie fest in C++."
type: docs
weight: 47000
url: /de/cpp/aspose.words/pagesetup/get_verticalalignment/
---
## PageSetup::get_VerticalAlignment method


Gibt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt zurück oder legt sie fest.

```cpp
Aspose::Words::PageVerticalAlignment Aspose::Words::PageSetup::get_VerticalAlignment()
```


## Beispiele



Zeigt, wie Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument angewendet und zurückgesetzt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Wenn wir einen neuen Abschnitt mit einem Dokument-Builder starten,
// erbt die aktuellen Seiteneinrichtungseigenschaften des Builders.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Wir können seine Seiteneinrichtungseigenschaften mit der Methode "ClearFormatting" auf die Standardwerte zurücksetzen.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Siehe auch

* Enum [PageVerticalAlignment](../../pageverticalalignment/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
