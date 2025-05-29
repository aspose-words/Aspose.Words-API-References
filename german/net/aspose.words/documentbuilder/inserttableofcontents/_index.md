---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der DocumentBuilder-Methode „InsertTableOfContents“ und fügen Sie ein dynamisches Inhaltsverzeichnis für eine einfache Navigation und verbesserte Organisation hinzu.
type: docs
weight: 500
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

Ein Inhaltsverzeichnis in einem Word-Dokument kann auf verschiedene Arten erstellt und mit verschiedenen Optionen formatiert werden. Die Art und Weise, wie die Tabelle in Microsoft Word erstellt und angezeigt wird, wird über die Feldschalter gesteuert.

Die einfachste Möglichkeit, die Schalter festzulegen, besteht darin, ein Inhaltsverzeichnis in ein Word-Dokument einzufügen und zu konfigurieren. Verwenden Sie dazu das Menü „Einfügen“ &gt; „Referenz“ &gt; „Index und Tabellen“. Aktivieren Sie anschließend die Anzeige der Feldfunktionen, um die Schalter anzuzeigen. In Microsoft Word können Sie die Anzeige der Feldfunktionen mit Alt+F9 ein- oder ausschalten.

Beispielsweise wird nach dem Erstellen eines Inhaltsverzeichnisses folgendes Feld in das Dokument eingefügt :**{ Inhaltsverzeichnis \o "1-3" \h \z \u }** . Sie können kopieren**\o "1-3" \h \z \u** und verwenden Sie es als Schalterparameter.

Beachten Sie, dass`InsertTableOfContents` fügt lediglich ein Inhaltsverzeichnisfeld ein, erstellt aber nicht das eigentliche Inhaltsverzeichnis. Das Inhaltsverzeichnis wird von Microsoft Word erstellt, wenn das Feld aktualisiert wird.

Wenn Sie mit dieser Methode ein Inhaltsverzeichnis einfügen und dann die Datei in Microsoft Word öffnen, wird das Inhaltsverzeichnis nicht angezeigt, da das Inhaltsverzeichnisfeld noch nicht aktualisiert wurde.

In Microsoft Word werden Felder beim Öffnen eines Dokuments nicht automatisch aktualisiert, Sie können Felder in einem Dokument jedoch jederzeit durch Drücken von F9 aktualisieren.

## Beispiele

Zeigt, wie Sie ein Inhaltsverzeichnis (TOC) in ein Dokument einfügen, indem Sie Überschriftenstile als Einträge verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Inhaltsverzeichnis für die erste Seite des Dokuments ein.
// Konfigurieren Sie die Tabelle so, dass Absätze mit Überschriften der Ebenen 1 bis 3 aufgenommen werden.
// Legen Sie außerdem fest, dass die Einträge Hyperlinks sind, die uns
// zur Position der Überschrift, wenn in Microsoft Word mit der linken Maustaste geklickt wird.
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
