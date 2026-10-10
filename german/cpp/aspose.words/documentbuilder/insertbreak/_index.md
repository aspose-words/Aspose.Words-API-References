---
title: "Aspose::Words::DocumentBuilder::InsertBreak Methode"
linktitle: "InsertBreak"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertBreak Methode. Fügt einen Umbruch des angegebenen Typs in das Dokument in C++ ein."
type: docs
weight: 28000
url: /de/cpp/aspose.words/documentbuilder/insertbreak/
---
## DocumentBuilder::InsertBreak method


Fügt einen Umbruch des angegebenen Typs in das Dokument ein.

```cpp
void Aspose::Words::DocumentBuilder::InsertBreak(Aspose::Words::BreakType breakType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| breakType | Aspose::Words::BreakType | Gibt den Typ des einzufügenden Umbruchs an. |

## Beispiele



Zeigt, wie man ein Inhaltsverzeichnis (TOC) in ein Dokument einfügt, indem man Überschriftenstile als Einträge verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein Inhaltsverzeichnis für die erste Seite des Dokuments ein.
// Konfigurieren Sie die Tabelle, um Absätze mit Überschriften der Ebenen 1 bis 3 zu erfassen.
// Stellen Sie außerdem ein, dass seine Einträge Hyperlinks sind, die uns
// zum Ort der Überschrift führen, wenn sie in Microsoft Word mit der linken Maustaste angeklickt werden.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftsformaten hinzufügen.
// Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erzeugt einen Eintrag in der Tabelle.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Ein Inhaltsverzeichnis ist ein Feld eines Typs, das aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


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

* Enum [BreakType](../../breaktype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
