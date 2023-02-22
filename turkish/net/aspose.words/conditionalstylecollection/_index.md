---
title: Class ConditionalStyleCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ConditionalStyleCollection sınıf. Bir koleksiyonu temsil ederConditionalStyle nesneler.
type: docs
weight: 310
url: /tr/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Bir koleksiyonu temsil eder[`ConditionalStyle`](../conditionalstyle/) nesneler.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Sol alt hücre stilini alır. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Sağ alttaki hücre stilini alır. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Koleksiyondaki koşullu stillerin sayısını alır. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Eşit sütun şeritleme stilini alır. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Eşit satır şeritleme stilini alır. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | İlk sütun stilini alır. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | İlk satır stilini alır. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Bir[`ConditionalStyle`](../conditionalstyle/) koşullu stil türüne göre nesne. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Son sütun stilini alır. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Son satır stilini alır. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Tek sütun şeritleme stilini alır. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Tek satır bantlama stilini alır. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Sol üst hücre stilini alır. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Sağ üst hücre stilini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Tablo stilinin tüm koşullu stillerini temizler. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Koleksiyondaki tüm koşullu stilleri yinelemek için kullanılabilecek bir numaralandırıcı nesnesi döndürür. |

### Notlar

Bu koleksiyona öğe eklemek veya bu koleksiyondan öğe çıkarmak mümkün değildir. Kalıcı öğe kümesi içerir: her bir değer için için bir öğe[`ConditionalStyleType`](../conditionalstyletype/) numaralandırma türü.

### Örnekler

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

// Koşullu stiller, tablo hücrelerinin yalnızca bazılarını etkileyen biçimlendirme değişiklikleridir.
// hücrelerin son satırda olması gibi bir yüklemi temel alır.
// Aşağıda, "ConditionalStyles" koleksiyonundan bir tablo stilinin koşullu stillerine erişmenin üç yolu bulunmaktadır.
// 1 - Stil türüne göre:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Dizine göre:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Özellik olarak:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Koşullu stillere dolgu ve metin biçimlendirme uygulayın.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Tüm olası stil koşullarını listeleyin.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Tüm koşullu stilleri içeren özel stili tabloya uygulayın.
table.Style = tableStyle;

// Stilimiz, varsayılan olarak bazı koşullu stilleri uygular.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// "StyleOptions" özelliği aracılığıyla diğer tüm stilleri kendimiz etkinleştirmemiz gerekecek.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Ayrıca bakınız

* class [ConditionalStyle](../conditionalstyle/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


