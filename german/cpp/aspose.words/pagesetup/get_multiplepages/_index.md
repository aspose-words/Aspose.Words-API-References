---
title: "Aspose::Words::PageSetup::get_MultiplePages-Methode"
linktitle: "get_MultiplePages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_MultiplePages Methode. Für mehrseitige Dokumente wird ermittelt oder festgelegt, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft in C++ gebunden werden kann."
type: docs
weight: 29000
url: /de/cpp/aspose.words/pagesetup/get_multiplepages/
---
## PageSetup::get_MultiplePages method


Für mehrseitige Dokumente liest oder legt fest, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft gebunden werden kann.

```cpp
Aspose::Words::Settings::MultiplePagesType Aspose::Words::PageSetup::get_MultiplePages() const
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


Zeigt, wie ein Dokument konfiguriert wird, das als Buchfalz gedruckt werden kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügt Text ein, der sich über 16 Seiten erstreckt.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Konfigurieren Sie die "PageSetup"-Eigenschaft des ersten Abschnitts, um das Dokument in Form eines Buchfalz zu drucken.
// Wenn wir dieses Dokument beidseitig drucken, können wir die Seiten nehmen, um sie zu stapeln
// und sie alle gleichzeitig in der Mitte falten. Der Inhalt des Dokuments wird zu einem Buchfalz ausgerichtet.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Wir können die Anzahl der Blätter nur in Vielfachen von 4 angeben.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Siehe auch

* Enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
