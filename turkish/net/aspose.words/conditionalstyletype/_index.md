---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words for .NET
description: Aspose.Words.ConditionalStyleType Sıralama. Bir tablo stilinde koşullu biçimlendirmenin tanımlanabileceği olası tablo alanlarını temsil eder C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Bir tablo stilinde koşullu biçimlendirmenin tanımlanabileceği olası tablo alanlarını temsil eder.

```csharp
public enum ConditionalStyleType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| FirstRow | `0` | Bir tablonun ilk satırının formatını belirtir. |
| FirstColumn | `1` | Bir tablonun ilk sütununun biçimlendirmesini belirtir. |
| LastRow | `2` | Tablonun son satırının formatını belirtir. |
| LastColumn | `3` | Bir tablonun son sütununun biçimlendirmesini belirtir. |
| OddRowBanding | `4` | Tek sayılı satır şeridinin formatını belirtir. |
| OddColumnBanding | `5` | Tek sayılı sütun şeridinin biçimlendirmesini belirtir. |
| EvenRowBanding | `6` | Çift sayılı satır şeridinin formatını belirtir. |
| EvenColumnBanding | `7` | Çift sayılı sütun şeridinin biçimlendirmesini belirtir. |
| TopLeftCell | `8` | Bir tablonun sol üst hücresinin biçimlendirmesini belirtir. |
| TopRightCell | `9` | Bir tablonun sağ üst hücresinin biçimlendirmesini belirtir. |
| BottomLeftCell | `10` | Bir tablonun sol alt hücresinin formatını belirtir. |
| BottomRightCell | `11` | Bir tablonun sağ alt hücresinin formatını belirtir. |

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
// hücrelerin son satırda olması gibi bir yüklemi temel alır.
// Aşağıda "ConditionalStyles" koleksiyonundan bir tablo stilinin koşullu stillerine erişmenin üç yolu verilmiştir.
// 1 - Stil türüne göre:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Dizine göre:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Özellik olarak:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Koşullu stillere dolgu ve metin biçimlendirmesi uygulayın.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Olası tüm stil koşullarını listeleyin.
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

// Stilimiz varsayılan olarak bazı koşullu stilleri uygular.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// "StyleOptions" özelliği aracılığıyla diğer tüm stilleri kendimiz etkinleştirmemiz gerekecek.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
