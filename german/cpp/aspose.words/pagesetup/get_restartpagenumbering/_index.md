---
title: "Aspose::Words::PageSetup::get_RestartPageNumbering Methode"
linktitle: "get_RestartPageNumbering"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_RestartPageNumbering Methode. Wahr, wenn die Seitennummerierung zu Beginn des Abschnitts in C++ neu startet."
type: docs
weight: 38000
url: /de/cpp/aspose.words/pagesetup/get_restartpagenumbering/
---
## PageSetup::get_RestartPageNumbering method


True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt.

```cpp
bool Aspose::Words::PageSetup::get_RestartPageNumbering()
```


## Beispiele



Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Verschieben Sie den Document Builder zum primären Header des ersten Abschnitts,
// der von jeder Seite dieses Abschnitts angezeigt wird.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Fügen Sie ein PAGE-Feld ein, das die Nummer der aktuellen Seite anzeigt.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Konfigurieren Sie den Abschnitt so, dass die von PAGE-Feldern angezeigte Seitenzahl bei 5 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass sie ihre Seitenzahlen mit Großbuchstaben‑römischen Ziffern anzeigen.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Erstellen Sie eine weitere primäre Kopfzeile für den zweiten Abschnitt, mit einem weiteren PAGE-Feld.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die PAGE-Felder anzeigen, bei 10 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass sie ihre Seitenzahlen mit arabischen Ziffern anzeigen.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
