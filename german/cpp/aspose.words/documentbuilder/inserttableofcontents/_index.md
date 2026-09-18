---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents Methode"
linktitle: "InsertTableOfContents"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents Methode. Fügt ein TOC (Inhaltsverzeichnis)-Feld in das Dokument in C++ ein."
type: docs
weight: 48000
url: /de/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Fügt ein TOC‑Feld (Inhaltsverzeichnis) in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Schalter | const System::String\& | Die Schalter des TOC-Feldes. |
## Hinweise


Diese Methode fügt ein TOC (Inhaltsverzeichnis)-Feld an der aktuellen Position in das Dokument ein.

Ein Inhaltsverzeichnis in einem Word-Dokument kann auf verschiedene Arten erstellt und mit einer Vielzahl von Optionen formatiert werden. Die Art, wie das Inhaltsverzeichnis von Microsoft Word erstellt und angezeigt wird, wird durch die Feldschalter gesteuert.

Der einfachste Weg, die Schalter anzugeben, besteht darin, ein Inhaltsverzeichnis in ein Word-Dokument einzufügen und zu konfigurieren, indem man das Menü Insert->Reference->Index und [Tables](../../../aspose.words.tables/) verwendet, dann die Anzeige von Feldcodes einschaltet, um die Schalter zu sehen. Sie können in Microsoft Word Alt+F9 drücken, um die Anzeige von Feldcodes ein- oder auszuschalten.

Zum Beispiel wird nach dem Erstellen eines Inhaltsverzeichnisses das folgende Feld in das Dokument eingefügt: **%{ TOC \o "1-3" \h \z }**. Sie können **%\o "1-3" \h \z** kopieren und als Schalter-Parameter verwenden.

Beachten Sie, dass [InsertTableOfContents()](../) nur ein TOC-Feld einfügt, aber das Inhaltsverzeichnis nicht tatsächlich erstellt. Das Inhaltsverzeichnis wird von Microsoft Word erstellt, wenn das Feld aktualisiert wird.

Wenn Sie mit dieser Methode ein Inhaltsverzeichnis einfügen und dann die Datei in Microsoft Word öffnen, wird das Inhaltsverzeichnis nicht angezeigt, weil das TOC-Feld noch nicht aktualisiert wurde.

In Microsoft Word werden Felder beim Öffnen eines Dokuments nicht automatisch aktualisiert, aber Sie können Felder jederzeit durch Drücken von F9 aktualisieren.

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

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
