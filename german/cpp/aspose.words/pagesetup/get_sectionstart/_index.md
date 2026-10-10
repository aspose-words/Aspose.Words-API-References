---
title: "Aspose::Words::PageSetup::get_SectionStart-Methode"
linktitle: "get_SectionStart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_SectionStart-Methode. Gibt den Typ des Abschnittsumbruchs für das angegebene Objekt zurück oder legt ihn fest in C++."
type: docs
weight: 41000
url: /de/cpp/aspose.words/pagesetup/get_sectionstart/
---
## PageSetup::get_SectionStart method


Gibt den Typ des Abschnittsumbruchs für das angegebene Objekt zurück oder legt ihn fest.

```cpp
Aspose::Words::SectionStart Aspose::Words::PageSetup::get_SectionStart()
```


## Beispiele



Zeigt, wie man angibt, wie ein neuer Abschnitt sich vom vorherigen trennt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// Abschnittswechseltypen bestimmen, wie ein neuer Abschnitt sich vom vorherigen Abschnitt trennt.
// Unten sind fünf Arten von Abschnittswechseln aufgeführt.
// 1 -  Beginnt den nächsten Abschnitt auf einer neuen Seite:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(Aspose::Words::SectionStart::NewPage, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());

// 2 -  Beginnt den nächsten Abschnitt auf der aktuellen Seite:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart());

// 3 -  Beginnt den nächsten Abschnitt auf einer neuen geraden Seite:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(Aspose::Words::SectionStart::EvenPage, doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart());

// 4 -  Beginnt den nächsten Abschnitt auf einer neuen ungeraden Seite:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(Aspose::Words::SectionStart::OddPage, doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart());

// 5 -  Beginnt den nächsten Abschnitt in einer neuen Spalte:
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(Aspose::Words::SectionStart::NewColumn, doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart());

doc->Save(get_ArtifactsDir() + u"PageSetup.SetSectionStart.docx");
```


Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und erhalten ein Dokumentenknoten ohne Kinder.
doc->RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
// Erstellen Sie zunächst einen neuen Abschnitt und fügen Sie ihn dann als Kind zum Wurzel-Dokumentenknoten hinzu.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt.
// auf der Seite zwischen der Kopf‑ und Fußzeile des Abschnitts.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Fügen Sie schließlich etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
// setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Siehe auch

* Enum [SectionStart](../../sectionstart/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
