---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.HeaderFooterType zur einfachen Identifizierung von Kopf- und Fußzeilentypen in Word-Dokumenten. Optimieren Sie Ihre Dokumentenverarbeitung noch heute!
type: docs
weight: 3550
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
| HeaderEven | `0` | Kopfzeile für gerade Seitenzahlen. |
| HeaderPrimary | `1` | Primäre Kopfzeile, wird auch für Seiten mit ungeraden Nummern verwendet. |
| FooterEven | `2` | Fußzeile für gerade Seitenzahlen. |
| FooterPrimary | `3` | Primäre Fußzeile, wird auch für Seiten mit ungeraden Nummern verwendet. |
| HeaderFirst | `4` | Kopfzeile für die erste Seite des Abschnitts. |
| FooterFirst | `5` | Fußzeile für die erste Seite des Abschnitts. |

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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
