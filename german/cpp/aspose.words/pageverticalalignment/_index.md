---
title: "Aspose::Words::PageVerticalAlignment‑Enum"
linktitle: "PageVerticalAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageVerticalAlignment‑Enum. Gibt die vertikale Ausrichtung des Textes auf jeder Seite in C++ an."
type: docs
weight: 108000
url: /de/cpp/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enum


Gibt die vertikale Ausrichtung des Textes auf jeder Seite an.

```cpp
enum class PageVerticalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unten | 3 | Der Text ist am unteren Rand der Seite ausgerichtet. |
| Mitte | 1 | Der Text ist in der Mitte der Seite ausgerichtet. |
| Blocksatz | 2 | Der Text wird verteilt, um die Seite zu füllen. |
| Oben | 0 | Der Text ist am oberen Rand der Seite ausgerichtet. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
