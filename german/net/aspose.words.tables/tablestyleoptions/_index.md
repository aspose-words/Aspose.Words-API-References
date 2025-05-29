---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Tables.TableStyleOptions für flexible Tabellengestaltung. Verbessern Sie Ihr Dokumentdesign noch heute mit anpassbaren Tabellenstilen!
type: docs
weight: 7220
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
| None | `0` | Es wird keine Tabellenformatierung angewendet. |
| FirstRow | `20` | Bedingte Formatierung auf die erste Zeile anwenden. |
| LastRow | `40` | Bedingte Formatierung auf die letzte Zeile anwenden. |
| FirstColumn | `80` | Bedingte Formatierung auf die erste Spalte anwenden. |
| LastColumn | `100` | Bedingte Formatierung der letzten Spalte anwenden. |
| RowBands | `200` | Bedingte Formatierung für Zeilenbänder anwenden. |
| ColumnBands | `400` | Bedingte Formatierung durch Spaltenbandbildung anwenden. |
| Default2003 | `600` | Zeilen- und Spaltenbandierung wird angewendet. Dies ist die Standardeinstellung von Microsoft Word für alte Formate wie DOC, WML und RTF. |
| Default | `2A0` | Dies sind die Standardeinstellungen von Microsoft Word. |

## Beispiele

Zeigt, wie beim Anwenden eines Stils eine neue Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Wir müssen mindestens eine Zeile einfügen, bevor wir eine Tabellenformatierung festlegen.
builder.InsertCell();

// Legen Sie den verwendeten Tabellenstil basierend auf der Stilkennung fest.
// Beachten Sie, dass beim Speichern im DOC-Format nicht alle Tabellenstile verfügbar sind.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Wenden Sie den Stil teilweise auf Funktionen der Tabelle basierend auf Prädikaten an und erstellen Sie dann die Tabelle.
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
