---
title: ConditionalStyleCollection.ClearFormatting
second_title: Aspose.Words for .NET API Referansı
description: ConditionalStyleCollection yöntem. Tablo stilinin tüm koşullu stillerini temizler.
type: docs
weight: 150
url: /tr/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Tablo stilinin tüm koşullu stillerini temizler.

```csharp
public void ClearFormatting()
```

### Örnekler

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

// Tablo stilini, tablonun ilk satırının kenarlıklarını kırmızı renklendirecek şekilde ayarlayın.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Tablo stilini, tablonun son satırının kenarlıklarını mavi renklendirecek şekilde ayarlayın.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Aşağıda, koşullu stilleri temizlemek için "ClearFormatting" yöntemini kullanmanın iki yolu verilmiştir.
// 1 - Tablonun belirli bir bölümü için koşullu stilleri temizleyin:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Tablonun tamamı için koşullu stilleri temizleyin:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Ayrıca bakınız

* class [ConditionalStyleCollection](../)
* ad alanı [Aspose.Words](../../conditionalstylecollection/)
* toplantı [Aspose.Words](../../../)


