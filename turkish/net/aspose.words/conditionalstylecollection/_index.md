---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: .NET için Aspose.Words
description: ConditionalStyle nesnelerini etkili bir şekilde yönetmek, belge biçimlendirmesini ve özelleştirmeyi geliştirmek için Aspose.Words.ConditionalStyleCollection sınıfını keşfedin.
type: docs
weight: 520
url: /tr/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Bir koleksiyonu temsil eder[`ConditionalStyle`](../conditionalstyle/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Tablolarla Çalışma](https://docs.aspose.com/words/net/working-with-tables/) belgeleme makalesi.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Sol alttaki hücre stilini alır. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Sağ alttaki hücre stilini alır. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Koleksiyondaki koşullu stillerin sayısını alır. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Eşit sütun bantlama stilini alır. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Çift satır bantlama stilini alır. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | İlk sütun stilini alır. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | İlk satır stilini alır. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Birini alır[`ConditionalStyle`](../conditionalstyle/) koşullu stil türüne göre nesne. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Son sütun stilini alır. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Son satır stilini alır. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Tek sütun bantlama stilini alır. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Tek satır bantlama stilini alır. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Sol üst hücre stilini alır. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Sağ üst hücre stilini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Tablo stilinin tüm koşullu stillerini temizler. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Koleksiyondaki tüm koşullu stiller üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |

## Notlar

Bu koleksiyona öğe eklemek veya kaldırmak mümkün değildir. Kalıcı öğe kümesi içerir: her değer için bir öğe [`ConditionalStyleType`](../conditionalstyletype/) numaralandırma türü.

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

* class [ConditionalStyle](../conditionalstyle/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
