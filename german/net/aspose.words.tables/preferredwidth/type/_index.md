---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: PreferredWidth Type eigendom. Ruft die Maßeinheit ab die für diesen bevorzugten Breitenwert verwendet wird in C#.
type: docs
weight: 40
url: /de/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Ruft die Maßeinheit ab, die für diesen bevorzugten Breitenwert verwendet wird.

```csharp
public PreferredWidthType Type { get; }
```

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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
