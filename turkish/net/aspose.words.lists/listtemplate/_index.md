---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words for .NET
description: Aspose.Words.Lists.ListTemplate Sıralama. Microsoft Wordde bulunan önceden tanımlanmış liste formatlarından birini belirtir C#'da.
type: docs
weight: 3530
url: /tr/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Microsoft Word'de bulunan önceden tanımlanmış liste formatlarından birini belirtir.

```csharp
public enum ListTemplate
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| BulletDefault | `0` | seviyeli varsayılan madde işaretli liste. Birinci düzeyin madde işareti bir disktir, ikinci düzeyin madde işareti bir dairedir, üçüncü düzeyin madde işareti bir karedir. Daha sonra biçimlendirme geri kalan düzeyler için tekrarlanır. |
| BulletDisk | `0` | İle aynıBulletDefault. |
| BulletCircle | `1` | Birinci seviyenin mermisi bir dairedir. Geriye kalan seviyeler öncekiyle aynıdır.BulletDefault. |
| BulletSquare | `2` | Birinci seviyenin mermisi karedir. Geriye kalan seviyeler öncekiyle aynıdır.BulletDefault. |
| BulletDiamonds | `3` | Birinci seviyenin mermisi 4 elmaslı Wingding karakteridir. Geriye kalan seviyeler öncekiyle aynıdır.BulletDefault. |
| BulletArrowHead | `4` | Birinci seviyenin mermisi ok uçlu Wingding karakteridir. Geriye kalan seviyeler öncekiyle aynıdır.BulletDefault. |
| BulletTick | `5` | Birinci seviyenin mermisi bir kene Wingding karakteridir. Geriye kalan seviyeler öncekiyle aynıdır.BulletDefault. |
| NumberDefault | `6` | 9 seviyeli varsayılan numaralandırılmış liste. Birinci düzey için Arapça numaralandırma (1., 2., 3., ...), ikinci düzey için küçük harf numaralandırma (a., b., c., ...), küçük harf roman numaralandırma (i) ., ii., iii., ...) üçüncü düzey için. Daha sonra biçimlendirme kalan düzeyler için tekrarlanır. |
| NumberArabicDot | `6` | İle aynıNumberDefault. |
| NumberArabicParenthesis | `7` | Birinci seviyenin numarası "1)"dir. Geriye kalan seviyeler öncekiyle aynıdır.NumberDefault. |
| NumberUppercaseRomanDot | `8` | Birinci seviyenin numarası "I"dir. Geriye kalan seviyeler öncekiyle aynıdır.NumberDefault. |
| NumberUppercaseLetterDot | `9` | Birinci seviyenin numarası "A"dır. Geriye kalan seviyeler öncekiyle aynıdır.NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Birinci seviyenin numarası "a)"dır. Geriye kalan seviyeler öncekiyle aynıdır.NumberDefault. |
| NumberLowercaseLetterDot | `11` | Birinci seviyenin numarası "a"dır. Geriye kalan seviyeler öncekiyle aynıdır.NumberDefault. |
| NumberLowercaseRomanDot | `12` | Birinci seviyenin numarası "i"dir. Geriye kalan seviyeler öncekiyle aynıdır.NumberDefault. |
| OutlineNumbers | `13` | "1), a), i), (1), (a), (i), 1., a., i." numaralı düzeylerden oluşan bir taslak liste. |
| OutlineLegal | `14` | Seviyeleri içeren taslak liste "1., 1.1., 1.1.1, ..." olarak numaralandırılmıştır. |
| OutlineBullets | `15` | Farklı düzeyler için çeşitli madde işaretlerinin yer aldığı bir taslak liste. |
| OutlineHeadingsArticleSection | `16` | Başlık stillerine bağlı seviyelerin yer aldığı bir taslak listesi. |
| OutlineHeadingsLegal | `17` | Başlık stillerine bağlı seviyelerin yer aldığı bir taslak listesi. |
| OutlineHeadingsNumbers | `18` | Başlık stillerine bağlı seviyelerin yer aldığı bir taslak listesi. |
| OutlineHeadingsChapter | `19` | Başlık stillerine bağlı seviyelerin yer aldığı bir taslak listesi. |

## Notlar

the 'de parametre olarak bir liste şablonu değeri kullanılır[`Add`](../listcollection/add/) yöntem.

Aspose.Words liste şablonları, Microsoft Word 2003'teki Madde İşaretleri ve Numaralandırma iletişim kutusunda bulunan 21 liste şablonuna karşılık gelir .

## Örnekler

Tüm ana hat başlıkları listesi şablonlarını içeren bir belgenin nasıl oluşturulacağını gösterir.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Bir listeyi kopyalayarak listedeki numaralandırmanın nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve ilk liste düzeyini özelleştirin.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Listemizi bazı paragraflara uygulayın.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Mevcut bir listenin bir kopyasını belgenin liste koleksiyonuna ekleyebiliriz
// orijinalde değişiklik yapmadan benzer bir liste oluşturmak için.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// İkinci listeyi yeni paragraflara uygula.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Liste düzeyleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Aşağıda belge oluşturucuyu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Numaralandırılmış bir liste:
// Numaralandırılmış listeler, her öğeyi numaralandırarak paragrafları için mantıksal bir düzen oluşturur.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// "ListLevelNumber" özelliğini ayarlayarak liste seviyesini arttırabiliriz
// geçerli liste öğesinde bağımsız bir alt liste başlatmak için.
// "NumberDefault" adı verilen Microsoft Word liste şablonu, ilk liste düzeyi için liste düzeyleri oluşturmak amacıyla sayıları kullanır.
 // Daha derin liste seviyelerinde harfler ve küçük harf Romen rakamları kullanılır.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Madde işaretli liste:
// Bu liste, her paragraftan önce bir girinti ve madde işareti simgesi ("•") uygulayacaktır.
// Bu listenin daha derin seviyelerinde "■" ve "○" gibi farklı semboller kullanılacaktır.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// "Liste" bayrağının ayarını kaldırarak sonraki paragrafları liste olarak biçimlendirmemek için liste biçimlendirmesini devre dışı bırakabiliriz.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
