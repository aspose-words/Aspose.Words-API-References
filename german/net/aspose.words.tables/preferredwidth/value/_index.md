---
title: PreferredWidth.Value
second_title: Aspose.Words für .NET-API-Referenz
description: PreferredWidth eigendom. Ruft den bevorzugten Breitenwert ab. Die Maßeinheit ist in der angegebenType Eigentum.
type: docs
weight: 50
url: /de/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Ruft den bevorzugten Breitenwert ab. Die Maßeinheit ist in der angegeben[`Type`](../type/) Eigentum.

```csharp
public double Value { get; }
```

### Beispiele

Zeigt, wie Sie den bevorzugten Breitentyp und -wert einer Tabellenzelle überprüfen.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Siehe auch

* class [PreferredWidth](../)
* namensraum [Aspose.Words.Tables](../../preferredwidth/)
* Montage [Aspose.Words](../../../)


