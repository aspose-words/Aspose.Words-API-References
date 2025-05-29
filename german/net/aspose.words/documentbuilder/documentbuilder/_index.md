---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos leistungsstarke Dokumente mit DocumentBuilder. Initialisieren Sie eine neue Instanz und optimieren Sie noch heute Ihr Dokumentenmanagement!
type: docs
weight: 10
url: /de/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public DocumentBuilder()
```

## Bemerkungen

Erstellt ein neues[`DocumentBuilder`](../)Objekt und hängt es an ein neues[`Document`](../../document/) Objekt.

## Beispiele

Zeigt, wie formatierter Text mit DocumentBuilder eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie die Schriftformatierung an und fügen Sie dann Text hinzu.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Bemerkungen

Erstellt ein neues[`DocumentBuilder`](../)Objekt und hängt es an ein neues[`Document`](../../document/) Objekt. Zusätzliche Optionen zum Erstellen von Dokumenten können angegeben werden.

## Beispiele

Zeigt, wie die Tabellenformatierung für den Inhalt danach ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Fügt Inhalt vor der Tabelle hinzu.
// Die Standardschriftgröße ist 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Ändert die Schriftgröße innerhalb der Tabelle.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Wenn ContextTableFormatting wahr ist, wird die Tabellenformatierung anschließend nicht auf den Inhalt angewendet.
// Wenn ContextTableFormatting falsch ist, wird die Tabellenformatierung anschließend auf den Inhalt angewendet.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Siehe auch

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public DocumentBuilder(Document doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | Document | Der[`Document`](../../document/) Objekt, an das angehängt werden soll. |

## Bemerkungen

Erstellt ein neues[`DocumentBuilder`](../) Objekt, hängt an das angegebene[`Document`](../../document/) Objekt. Der Cursor wird an den Anfang des Dokuments positioniert.

## Beispiele

Zeigt, wie Sie mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir für die erste, die gerade und die ungerade Seite unterschiedliche Kopf- und Fußzeilen wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dem Dokument dann drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

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

* class [Document](../../document/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | Document | Der[`Document`](../../document/) Objekt, an das angehängt werden soll. |
| options | DocumentBuilderOptions | Zusätzliche Optionen für den Dokumenterstellungsprozess. |

## Bemerkungen

Erstellt ein neues[`DocumentBuilder`](../) Objekt, hängt an das angegebene[`Document`](../../document/) Objekt. Der Cursor wird an den Anfang des Dokuments positioniert.

## Beispiele

Zeigt, wie die Tabellenformatierung für den Inhalt danach ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Fügt Inhalt vor der Tabelle hinzu.
// Die Standardschriftgröße ist 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Ändert die Schriftgröße innerhalb der Tabelle.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Wenn ContextTableFormatting wahr ist, wird die Tabellenformatierung anschließend nicht auf den Inhalt angewendet.
// Wenn ContextTableFormatting falsch ist, wird die Tabellenformatierung anschließend auf den Inhalt angewendet.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Siehe auch

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
