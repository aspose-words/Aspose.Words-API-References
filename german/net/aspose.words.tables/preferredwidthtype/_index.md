---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words für .NET
description: Aspose.Words.Tables.PreferredWidthType opsomming. Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle an in C#.
type: docs
weight: 6300
url: /de/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle an.

```csharp
public enum PreferredWidthType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | `1` | Die bevorzugte Breite ist nicht angegeben. Die tatsächliche Breite der Tabelle oder Zelle wird entweder mithilfe der expliziten Breite angegeben oder wird automatisch vom Tabellenlayout-Algorithmus bestimmt, wenn die Tabelle angezeigt wird, abhängig von der Einstellung für die automatische Tabellenanpassung. |
| Percent | `2` | Messen Sie die aktuelle Artikelbreite mit einem angegebenen Prozentsatz. |
| Points | `3` | Messen Sie die aktuelle Artikelbreite anhand einer angegebenen Anzahl von Punkten (1/72 Zoll). |

## Beispiele

Zeigt, wie Sie den bevorzugten Breitentyp und Wert einer Tabellenzelle überprüfen.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Siehe auch

* class [PreferredWidth](../preferredwidth/)
* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
