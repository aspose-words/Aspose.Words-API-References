---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: .NET için Aspose.Words
description: FieldStart'ın FieldData özelliğiyle özel alan verilerinin kilidini açın, veri yönetiminizi geliştirin ve üretkenliğinizi zahmetsizce artırın.
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
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### Ayrıca bakınız

* class [FieldStart](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
