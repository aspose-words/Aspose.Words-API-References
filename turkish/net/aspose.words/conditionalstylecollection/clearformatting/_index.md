---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: .NET için Aspose.Words
description: ConditionalStyleCollection ClearFormatting yönteminin tablonuzdan tüm koşullu stilleri nasıl etkili bir şekilde kaldırdığını, netliği ve tasarımı nasıl geliştirdiğini keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Tablo stilinin tüm koşullu stillerini temizler.

```csharp
public void ClearFormatting()
```

## Örnekler

Koşullu tablo stillerinin nasıl sıfırlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Tablo stilini, tablonun ilk satırının kenarlıklarını kırmızı renkle renklendirecek şekilde ayarlayın.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Tablonun son satırının kenarlıklarını mavi renkle renklendirmek için tablo stilini ayarlayın.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Aşağıda koşullu stilleri temizlemek için "ClearFormatting" metodunu kullanmanın iki yolu bulunmaktadır.
// 1 - Tablonun belirli bir kısmı için koşullu stilleri temizle:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Tüm tablo için koşullu stilleri temizle:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Ayrıca bakınız

* class [ConditionalStyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
