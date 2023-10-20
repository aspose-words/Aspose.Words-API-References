---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words für .NET
description: Aspose.Words.HeaderFooterType opsomming. Identifiziert den Typ der Kopf oder Fußzeile in einer WordDatei in C#.
type: docs
weight: 3120
url: /de/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Identifiziert den Typ der Kopf- oder Fußzeile in einer Word-Datei.

```csharp
public enum HeaderFooterType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| HeaderEven | `0` | Kopfzeile für gerade nummerierte Seiten. |
| HeaderPrimary | `1` | Primärer Header, wird auch für Seiten mit ungeraden Seitenzahlen verwendet. |
| FooterEven | `2` | Fußzeile für gerade nummerierte Seiten. |
| FooterPrimary | `3` | Primäre Fußzeile, wird auch für Seiten mit ungeraden Seitenzahlen verwendet. |
| HeaderFirst | `4` | Kopfzeile für die erste Seite des Abschnitts. |
| FooterFirst | `5` | Fußzeile für die erste Seite des Abschnitts. |

## Beispiele

Zeigt, wie man mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir unterschiedliche Kopf- und Fußzeilen für die erste, gerade und ungerade Seite wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dann drei Seiten zum Dokument hinzu, um jeden Kopfzeilentyp anzuzeigen.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
