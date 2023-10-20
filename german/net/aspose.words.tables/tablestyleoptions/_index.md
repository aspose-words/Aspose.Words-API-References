---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Tables.TableStyleOptions opsomming. Gibt an wie der Tabellenstil auf eine Tabelle angewendet wird in C#.
type: docs
weight: 6370
url: /de/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Gibt an, wie der Tabellenstil auf eine Tabelle angewendet wird.

```csharp
[Flags]
public enum TableStyleOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Es wird keine Formatierung im Tabellenstil angewendet. |
| FirstRow | `20` | Bedingte Formatierung der ersten Zeile anwenden. |
| LastRow | `40` | Bedingte Formatierung der letzten Zeile anwenden. |
| FirstColumn | `80` | Wenden Sie die bedingte Formatierung der ersten Spalte an. |
| LastColumn | `100` | Bedingte Formatierung der letzten Spalte anwenden. |
| RowBands | `200` | Bedingte Zeilenbandformatierung anwenden. |
| ColumnBands | `400` | Wenden Sie die bedingte Formatierung der Spaltenbänder an. |
| Default2003 | `600` | Zeilen- und Spaltenbänderung wird angewendet. Dies ist die Microsoft Word-Standardeinstellung für alte Formate wie DOC, WML und RTF. |
| Default | `2A0` | Dies sind die Standardeinstellungen von Microsoft Word. |

## Beispiele

Zeigt, wie man eine neue Tabelle erstellt und dabei einen Stil anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Wir müssen mindestens eine Zeile einfügen, bevor wir eine Tabellenformatierung festlegen.
builder.InsertCell();

// Legen Sie den verwendeten Tabellenstil basierend auf der Stilkennung fest.
// Beachten Sie, dass beim Speichern im .doc-Format nicht alle Tabellenstile verfügbar sind.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Den Stil basierend auf Prädikaten teilweise auf Features der Tabelle anwenden und dann die Tabelle erstellen.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Siehe auch

* property [StyleOptions](../table/styleoptions/)
* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
