---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words for .NET
description: FieldStart FieldData mülk. Alanla ilişkili özel alan verilerini alır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Alanla ilişkili özel alan verilerini alır.

```csharp
public byte[] FieldData { get; }
```

## Örnekler

Alanla ilişkili verilerin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Ayrıca bakınız

* class [FieldStart](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
