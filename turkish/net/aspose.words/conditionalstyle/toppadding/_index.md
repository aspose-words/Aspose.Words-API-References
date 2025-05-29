---
title: ConditionalStyle.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: .NET için Aspose.Words
description: Daha iyi tasarım için tablo hücresi içeriklerinin üstündeki boşluğu kolayca ayarlamak, düzeni ve okunabilirliği geliştirmek için ConditionalStyle TopPadding özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words/conditionalstyle/toppadding/
---
## ConditionalStyle.TopPadding property

Tablo hücrelerinin içeriklerinin üstüne eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar.

```csharp
public double TopPadding { get; set; }
```

## Örnekler

Bir tablonun belirli alan stilleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Özel bir tablo stili oluşturun.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Koşullu stiller, tablonun yalnızca bazı hücrelerini etkileyen biçimlendirme değişiklikleridir
// hücrelerin son satırda olması gibi bir öngörüye dayalı.
// Aşağıda "ConditionalStyles" koleksiyonundan bir tablo stilinin koşullu stillerine erişmenin üç yolu bulunmaktadır.
// 1 - Stil türüne göre:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Dizin olarak:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Bir özellik olarak:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Koşullu stillere dolgu ve metin biçimlendirmesi uygulayın.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Tüm olası stil koşullarını listele.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Tüm koşullu stilleri içeren özel stili tabloya uygula.
table.Style = tableStyle;

// Stilimiz varsayılan olarak bazı koşullu stilleri uygular.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Diğer tüm stilleri "StyleOptions" özelliği aracılığıyla kendimiz etkinleştirmemiz gerekecek.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Ayrıca bakınız

* class [ConditionalStyle](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
