---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.TextColumn-Klasse zur Verwaltung von Textspalten in Ihren Dokumenten. Greifen Sie einfach auf jede Spalte in Ihrem Textabschnitt zu und passen Sie sie an.
type: docs
weight: 7240
url: /de/net/aspose.words/textcolumn/
---
## TextColumn class

Stellt eine einzelne Textspalte dar.`TextColumn` ist Mitglied der[`TextColumnCollection`](../textcolumncollection/) Sammlung. Die`TextColumn`Die Sammlung umfasst alle Spalten in einem Abschnitt eines Dokuments.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Abschnitten](https://docs.aspose.com/words/net/working-with-sections/) Dokumentationsartikel.

```csharp
public class TextColumn
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Ruft den Abstand zwischen dieser und der nächsten Spalte in Punkten ab oder legt ihn fest. Für die letzte Spalte ist dies nicht erforderlich. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Ruft die Breite der Textspalte in Punkten ab oder legt sie fest. |

## Bemerkungen

`TextColumn` Objekte werden nur verwendet, um Spalten mit benutzerdefinierter Breite und Abstand anzugeben. Wenn Sie möchten, dass die Spalten im Dokument gleich breit sind, legen Sie TextColumns fest.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) Zu`WAHR`.

Wenn ein neuer`TextColumn` erstellt wird, sind Breite und Abstand auf Null gesetzt.

## Beispiele

Zeigt, wie Spalten mit ungleichmäßigem Abstand erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Bestimmen Sie, wie viel Platz uns zum Anordnen der Spalten zur Verfügung steht.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Legen Sie fest, dass die erste Spalte schmal ist.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Stellen Sie die zweite Spalte so ein, dass sie den restlichen verfügbaren Platz innerhalb der Seitenränder einnimmt.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
