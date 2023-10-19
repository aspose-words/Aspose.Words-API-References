---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words for .NET
description: TableStyle ColumnStripe mülk. Stil tek/çift sütun bantlamasını belirttiğinde bantlamaya dahil edilecek sütun sayısını alır veya ayarlar C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Stil tek/çift sütun bantlamasını belirttiğinde, bantlamaya dahil edilecek sütun sayısını alır veya ayarlar.

```csharp
public int ColumnStripe { get; set; }
```

## Örnekler

Satırlar arasında geçiş yapan koşullu tablo stillerinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Satıra/sütuna farklı bir renk uygulamak için bir tablonun koşullu stilini yapılandırabiliriz,
// satırın/sütunun çift veya tek olmasına bağlı olarak alternatif bir renk deseni oluşturulur.
// Satır/sütun bantlamasına da n sayısını uygulayabiliriz,
// rengin bir yerine her n satır/sütun sonrasında değişeceği anlamına gelir.
// Tek sütunların ve satırların bantlanacağı, sütunların üçlü bantlanacağı bir tablo oluşturun.
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

// Tablonun tüm kenarlarına çizgi stili uygulayın.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Her 3 satırda bir değişecek olan iki rengi ayarlayın.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Her çift sütuna uygulanacak, özel satır renklendirmesini geçersiz kılacak bir renk belirleyin.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// "StyleOptions" özelliği varsayılan olarak satır bantlamayı etkinleştirir.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Sütun bantlamayı etkinleştirmek için "StyleOptions" özelliğini de kullanın.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Ayrıca bakınız

* class [TableStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
