---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words für .NET
description: DocumentBuilder MoveToSection methode. Bewegt den Cursor an den Anfang des Körpers in einem angegebenen Abschnitt in C#.
type: docs
weight: 570
url: /de/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Bewegt den Cursor an den Anfang des Körpers in einem angegebenen Abschnitt.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sectionIndex | Int32 | Der Index des Abschnitts, zu dem verschoben werden soll. |

## Bemerkungen

Wann*sectionIndex* größer oder gleich 0 ist, gibt es einen Index vom Anfang des Dokuments an, wobei 0 der erste Abschnitt ist. Wann*sectionIndex* kleiner als 0, ist, wurde ein Index vom Ende des Dokuments angegeben, wobei -1 der letzte Abschnitt ist.

Der Cursor wird zum ersten Absatz im verschoben[`Body`](../../body/) des angegebenen Abschnitts.

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

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
