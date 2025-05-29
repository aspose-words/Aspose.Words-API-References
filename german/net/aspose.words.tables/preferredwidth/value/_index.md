---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words für .NET
description: Entdecken Sie die PreferredWidth-Werteigenschaft, um Ihre bevorzugte Breite einfach anzupassen. Verbessern Sie Ihr Design noch heute mit präzisen Maßangaben!
type: docs
weight: 50
url: /de/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Ruft den gewünschten Breitenwert ab. Die Maßeinheit wird in der[`Type`](../type/) Eigenschaft.

```csharp
public double Value { get; }
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

* class [PreferredWidth](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
