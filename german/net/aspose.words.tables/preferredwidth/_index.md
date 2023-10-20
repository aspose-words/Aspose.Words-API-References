---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words für .NET
description: Aspose.Words.Tables.PreferredWidth klas. Stellt einen Wert und seine Maßeinheit dar die zur Angabe der bevorzugten Breite einer Tabelle oder Zelle verwendet wird in C#.
type: docs
weight: 6290
url: /de/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Stellt einen Wert und seine Maßeinheit dar, die zur Angabe der bevorzugten Breite einer Tabelle oder Zelle verwendet wird.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Tabellen](https://docs.aspose.com/words/net/working-with-tables/) Dokumentationsartikel.

```csharp
public sealed class PreferredWidth
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Ruft die Maßeinheit ab, die für diesen bevorzugten Breitenwert verwendet wird. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Ruft den bevorzugten Breitenwert ab. Die Maßeinheit ist im angegeben[`Type`](./type/) Eigenschaft. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | Eine Erstellungsmethode, die eine neue Instanz zurückgibt, die eine bevorzugte Breite darstellt, die als Prozentsatz angegeben wird. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | Eine Erstellungsmethode, die eine neue Instanz zurückgibt, die eine bevorzugte Breite darstellt, die mithilfe einer Anzahl von Punkten angegeben wird. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Bestimmt, ob die angegebene`PreferredWidth` ist vom Wert her gleich dem Strom`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Gibt eine benutzerfreundliche Zeichenfolge zurück, die den Wert dieses Objekts anzeigt. |

## Felder

| Name | Beschreibung |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Gibt eine Instanz zurück, die den Wert „Bevorzugte Breite ist nicht angegeben“ darstellt. |

## Bemerkungen

Die bevorzugte Breite kann als Prozentsatz, Anzahl der Punkte oder als spezieller „Keine/Auto“-Wert angegeben werden.

Die Instanzen dieser Klasse sind unveränderlich.

## Beispiele

Zeigt, wie man eine Tabelle so einstellt, dass sie automatisch an 50 % der Seitenbreite angepasst wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Zeigt, wie man eine bevorzugte Breite für Tabellenzellen festlegt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Es gibt zwei Möglichkeiten, die Klasse „PreferredWidth“ auf Tabellenzellen anzuwenden.
// 1 – Legen Sie eine absolute bevorzugte Breite basierend auf Punkten fest:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 – Legen Sie eine relative bevorzugte Breite basierend auf dem Prozentsatz der Tabellenbreite fest:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Eine Zelle, für die keine bevorzugte Breite angegeben ist, nimmt den Rest des verfügbaren Platzes ein.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Jede Konfiguration der Eigenschaft „PreferredWidth“ erstellt ein neues Objekt.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
