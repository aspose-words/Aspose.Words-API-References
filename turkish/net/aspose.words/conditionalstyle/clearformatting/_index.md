---
title: ConditionalStyle.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: .NET için Aspose.Words
description: ConditionalStyle ClearFormatting yöntemi ile zahmetsizce net biçimlendirme. Tasarım sürecinizi basitleştirin ve belge netliğini bugün artırın!
type: docs
weight: 100
url: /tr/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

Bu koşullu stilin biçimlendirmesini temizler.

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

* class [ConditionalStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
