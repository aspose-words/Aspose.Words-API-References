---
title: "Aspose::Words::PageSetup::get_RtlGutter‑Methode"
linktitle: "get_RtlGutter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_RtlGutter‑Methode. Gibt an oder legt fest, ob Microsoft Word für den Abschnitt Rinne (Gutter) basierend auf einer Rechts‑nach‑Links‑ oder Links‑nach‑Rechts‑Sprache verwendet in C++."
type: docs
weight: 40000
url: /de/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Liest oder legt fest, ob Microsoft Word für den Abschnitt Ränder basierend auf einer Rechts-nach-Links- oder Links-nach-Rechts-Sprache verwendet.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
```


## Beispiele



Zeigt, wie Gutter-Ränder eingestellt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie Text ein, der sich über mehrere Seiten erstreckt.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Ein Gutter fügt Leerzeichen entweder am linken oder rechten Seitenrand hinzu,
// was die zentrale Falz von Seiten in einem Buch ausgleicht, die in das Layout der Seite eingreift.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Bestimmen Sie, wie viel Platz unsere Seiten für Text innerhalb der Ränder haben, und fügen Sie dann einen Betrag hinzu, um einen Rand zu polstern.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Setzen Sie die Eigenschaft "RtlGutter" auf "true", um den Gutter für Rechts-nach-Links-Text an einer geeigneteren Position zu platzieren.
pageSetup->set_RtlGutter(true);

// Setzen Sie die Eigenschaft "MultiplePages" auf "MultiplePagesType.MirrorMargins", um abwechselnd
// die linke/rechte Seitenrandposition bei jedem Blatt zu ändern.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
