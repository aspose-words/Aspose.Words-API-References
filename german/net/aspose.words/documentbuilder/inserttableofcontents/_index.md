---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertTableOfContents methode. Fügt ein TOCFeld Inhaltsverzeichnis in das Dokument ein in C#.
type: docs
weight: 460
url: /de/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Fügt ein TOC-Feld (Inhaltsverzeichnis) in das Dokument ein.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| switches | String | Das TOC-Feld wechselt. |

## Bemerkungen

Diese Methode fügt an der aktuellen Position ein TOC-Feld (Inhaltsverzeichnis) in das Dokument ein.

Ein Inhaltsverzeichnis in einem Word-Dokument kann auf verschiedene Arten erstellt und mit verschiedenen Optionen formatiert werden. Die Art und Weise, wie die Tabelle von Microsoft Word erstellt und angezeigt wird, wird durch die Feldschalter gesteuert.

Der einfachste Weg, die Schalter anzugeben, besteht darin, über das Menü „Einfügen-&gt;Referenz-&gt;Index und Tabellen“ ein Inhaltsverzeichnis in ein Word-Dokument einzufügen und zu konfigurieren und dann die Anzeige der Feldcodes einzuschalten, um die Schalter anzuzeigen. Sie können Alt+F9 in Microsoft Word drücken, um die Anzeige von Feldcodes ein- oder auszuschalten.

Nach dem Erstellen eines Inhaltsverzeichnisses wird beispielsweise das folgende Feld in das Dokument eingefügt :**{ TOC \o "1-3" \h \z \u }** . Sie können kopieren**\o "1-3" \h \z \u** und verwenden Sie es als Schalterparameter.

Beachten Sie, dass`InsertTableOfContents` fügt nur ein TOC-Feld ein, aber erstellt nicht tatsächlich das Inhaltsverzeichnis. Das Inhaltsverzeichnis wird von Microsoft Word erstellt, wenn das Feld aktualisiert wird.

Wenn Sie mit dieser Methode ein Inhaltsverzeichnis einfügen und dann die Datei in Microsoft Word öffnen, wird das Inhaltsverzeichnis nicht angezeigt, da das Inhaltsverzeichnisfeld noch nicht aktualisiert wurde.

In Microsoft Word werden Felder beim Öffnen eines Dokuments nicht automatisch aktualisiert, Sie können Felder in einem Dokument jedoch jederzeit aktualisieren, indem Sie F9 drücken.

## Beispiele

Zeigt, wie man ein Inhaltsverzeichnis (TOC) in ein Dokument einfügt, indem man Überschriftenstile als Einträge verwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Inhaltsverzeichnis für die erste Seite des Dokuments einfügen.
// Konfigurieren Sie die Tabelle so, dass sie Absätze mit Überschriften der Ebenen 1 bis 3 aufnimmt.
// Legen Sie außerdem fest, dass seine Einträge Hyperlinks sind, die uns weiterleiten
// zur Position der Überschrift, wenn in Microsoft Word mit der linken Maustaste darauf geklickt wird.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftenstilen hinzufügen.
// Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erstellt einen Eintrag in der Tabelle.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Ein Inhaltsverzeichnis ist ein Feld eines Typs, der aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
