---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die MoveToSection-Methode von DocumentBuilder, um einfach zum Anfang des Hauptteils eines beliebigen Abschnitts zu navigieren und so die Effizienz Ihrer Dokumentbearbeitung zu steigern.
type: docs
weight: 610
url: /de/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Verschiebt den Cursor an den Anfang des Textkörpers in einem angegebenen Abschnitt.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sectionIndex | Int32 | Der Index des Abschnitts, zu dem verschoben werden soll. |

## Bemerkungen

Wann*sectionIndex*größer oder gleich 0 ist, gibt es einen Index von zum Anfang des Dokuments an, wobei 0 der erste Abschnitt ist. Wenn*sectionIndex* ist kleiner als 0, , es wurde ein Index vom Ende des Dokuments angegeben, wobei -1 der letzte Abschnitt ist.

Der Cursor wird zum ersten Absatz im[`Body`](../../body/) des angegebenen Abschnitts.

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

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
