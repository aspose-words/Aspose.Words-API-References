---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Tables.PreferredWidthType-enum. Definiera enkelt tabell- och cellbreddmått för exakt dokumentformatering.
type: docs
weight: 7150
url: /sv/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Anger måttenheten för den önskade bredden på en tabell eller cell.

```csharp
public enum PreferredWidthType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `1` | Den önskade bredden anges inte. Tabellens eller cellens faktiska bredd anges antingen med den explicita bredden eller så bestäms automatiskt av tabellens layoutalgoritm när tabellen visas, beroende på tabellens inställning för automatisk anpassning. |
| Percent | `2` | Mät den aktuella objektbredden med en angiven procentandel. |
| Points | `3` | Mät den aktuella objektbredden med ett angivet antal punkter (1/72 tum). |

## Exempel

Visar hur man verifierar önskad breddtyp och värde för en tabellcell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Se även

* class [PreferredWidth](../preferredwidth/)
* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
