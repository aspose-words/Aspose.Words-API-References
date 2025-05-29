---
title: TableStyle.RowStripe
linktitle: RowStripe
articleTitle: RowStripe
second_title: .NET için Aspose.Words
description: Gelişmiş tablo okunabilirliği ve görsel çekicilik için tek/çift satır bantlarını kolayca özelleştirmek üzere TableStyle RowStripe özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words/tablestyle/rowstripe/
---
## TableStyle.RowStripe property

Stil tek/çift satır bantlamasını belirttiğinde bantlamaya dahil edilecek satır sayısını alır veya ayarlar.

```csharp
public int RowStripe { get; set; }
```

## Örnekler

Satırlar arasında dönüşümlü koşullu tablo stilleri oluşturmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir tablonun satır/sütununa farklı bir renk uygulamak için koşullu bir stilini yapılandırabiliriz,
// satır/sütunun çift ya da tek olmasına göre değişen renk deseni oluşturur.
// Satır/sütun bantlamasına n sayısını da uygulayabiliriz,
// yani renk her n satır/sütun sonrasında bir yerine dönüşümlü olarak değişir.
// Tek sütunların ve satırların sütunları üçlü olarak bantlayacağı bir tablo oluşturun.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Tablonun tüm kenarlarına bir çizgi stili uygula.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Her 3 satırda dönüşümlü olacak iki rengi ayarlayın.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Her çift sütuna uygulanacak bir renk ayarlayın; bu, özel satır renklendirmesini geçersiz kılacaktır.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// "StyleOptions" özelliği varsayılan olarak satır bantlamasını etkinleştirir.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Sütun bantlamasını etkinleştirmek için "StyleOptions" özelliğini de kullanın.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Ayrıca bakınız

* class [TableStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
