---
title: Class TextColumn
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.TextColumn klas. Stellt eine einzelne Textspalte dar.TextColumn ist Mitglied derTextColumnCollection Sammlung. DieTextColumn Die Sammlung umfasst alle Spalten in einem Abschnitt eines Dokuments.
type: docs
weight: 6390
url: /de/net/aspose.words/textcolumn/
---
## TextColumn class

Stellt eine einzelne Textspalte dar.`TextColumn` ist Mitglied der[`TextColumnCollection`](../textcolumncollection/) Sammlung. Die`TextColumn` Die Sammlung umfasst alle Spalten in einem Abschnitt eines Dokuments.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Abschnitten](https://docs.aspose.com/words/net/working-with-sections/) Dokumentationsartikel.

```csharp
public class TextColumn
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Ruft den Abstand zwischen dieser Spalte und der nächsten Spalte in Punkten ab oder legt diesen fest. Für die letzte Spalte nicht erforderlich. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Ruft die Breite der Textspalte in Punkten ab oder legt sie fest. |

### Bemerkungen

`TextColumn` Objekte werden nur verwendet, um Spalten mit benutzerdefinierter Breite und benutzerdefiniertem Abstand anzugeben. Wenn Sie möchten, dass die Spalten im Dokument die gleiche Breite haben, legen Sie TextColumns fest.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) Zu`WAHR`.

Wenn ein neues`TextColumn` erstellt wird, werden Breite und Abstand auf Null gesetzt.

### Beispiele

Zeigt, wie ungleichmäßig verteilte Spalten erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Bestimmen Sie den verfügbaren Platz für die Anordnung der Spalten.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Setze die erste Spalte auf schmal.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Legen Sie die zweite Spalte so fest, dass sie den Rest des verfügbaren Platzes innerhalb der Seitenränder einnimmt.
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


