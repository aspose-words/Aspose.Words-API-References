---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter Methode"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter Methode. Wahr, wenn das Dokument unterschiedliche Kopf‑ und Fußzeilen für ungerade und gerade Seiten in C++ hat."
type: docs
weight: 30000
url: /de/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Wahr, wenn das Dokument unterschiedliche Kopf- und Fußzeilen für ungerade und gerade Seiten hat.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Beispiele



Zeigt, wie Kopf‑ und Fußzeilen für gerade Seiten aktiviert oder deaktiviert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Arten von Kopf‑/Fußzeilen aufgeführt.
// 1 -  Der "Primary" Header/Fußzeile, der auf jeder Seite im Abschnitt erscheint.
// Wir können den primären Header/Fußzeile durch einen ersten und einen geraden Seiten-Header/Fußzeile überschreiben.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  Der "Even" Header/Fußzeile, der auf jeder geraden Seite dieses Abschnitts erscheint.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Jeder Abschnitt hat ein "PageSetup"-Objekt, das seitenbezogene Erscheinungs‑Eigenschaften festlegt.
// wie Ausrichtung, Größe und Ränder.
// Setzen Sie die "OddAndEvenPagesHeaderFooter"‑Eigenschaft auf "true"
// um die gerade Seiten‑Header/Fußzeile auf geraden Seiten anzuzeigen.
// Setzen Sie die "OddAndEvenPagesHeaderFooter"‑Eigenschaft auf "false"
// um die primäre Header/Fußzeile auf geraden Seiten anzuzeigen.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
