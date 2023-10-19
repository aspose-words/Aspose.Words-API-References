---
title: ConditionalStyle.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: ConditionalStyle ClearFormatting yöntem. Bu koşullu stilin biçimlendirmesini temizler C#'da.
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

* class [ConditionalStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
