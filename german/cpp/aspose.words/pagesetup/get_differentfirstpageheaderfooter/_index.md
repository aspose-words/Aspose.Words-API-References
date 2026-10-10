---
title: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter Methode"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter Methode. true, wenn auf der ersten Seite ein anderer Kopf- oder Fußzeile verwendet wird in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


Wahr, wenn auf der ersten Seite eine andere Kopf- oder Fußzeile verwendet wird.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Beispiele



Zeigt, wie primäre Kopf‑ und Fußzeilen aktiviert oder deaktiviert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Arten von Kopf‑/Fußzeilen aufgeführt.
// 1 -  Die "First" Kopf-/Fußzeile, die auf der ersten Seite des Abschnitts erscheint.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  Die "Primary" Kopf-/Fußzeile, die auf jeder Seite des Abschnitts erscheint.
// Wir können den primären Header/Fußzeile durch einen ersten und einen geraden Seiten-Header/Fußzeile überschreiben.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Jeder Abschnitt hat ein "PageSetup"-Objekt, das seitenbezogene Erscheinungs‑Eigenschaften festlegt.
// wie Ausrichtung, Größe und Ränder.
// Setzen Sie die Eigenschaft "DifferentFirstPageHeaderFooter" auf "true", um die erste Kopf‑/Fußzeile auf der ersten Seite anzuwenden.
// Setzen Sie die Eigenschaft "DifferentFirstPageHeaderFooter" auf "false"
// um die erste Seite die primäre Kopf‑/Fußzeile anzeigen zu lassen.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
