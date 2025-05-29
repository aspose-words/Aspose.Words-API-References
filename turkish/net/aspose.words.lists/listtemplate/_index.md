---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: .NET için Aspose.Words
description: Belgenizin sunumunu zahmetsizce geliştirmek için önceden tanımlanmış Microsoft Word liste biçimlerini içeren Aspose.Words.Lists.ListTemplate enum'unu keşfedin.
type: docs
weight: 3980
url: /tr/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Microsoft Word'de bulunan önceden tanımlanmış liste biçimlerinden birini belirtir.

```csharp
public enum ListTemplate
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| BulletDefault | `0` | 9 seviyeli varsayılan madde işaretli liste. İlk seviyenin madde işareti bir disktir, ikinci seviyenin madde işareti bir dairedir, üçüncü seviyenin madde işareti bir karedir. Daha sonra biçimlendirme kalan seviyeler için tekrarlanır. |
| BulletDisk | `0` | AynısıBulletDefault. |
| BulletCircle | `1` | İlk seviyenin mermisi bir dairedir. Kalan seviyeler şu şekildedir:BulletDefault. |
| BulletSquare | `2` | İlk seviyenin mermisi karedir. Kalan seviyeler de aynıdırBulletDefault. |
| BulletDiamonds | `3` | İlk seviyenin mermisi 4 elmaslı bir Wingding karakteridir. Kalan seviyeler şu şekildedir:BulletDefault. |
| BulletArrowHead | `4` | İlk seviyenin mermisi ok uçlu bir Wingding karakteridir. Kalan seviyeler şu şekildedir:BulletDefault. |
| BulletTick | `5` | İlk seviyenin mermisi bir tick Wingding karakteridir. Kalan seviyeler şu şekildedir:BulletDefault. |
| NumberDefault | `6` | seviyeli varsayılan numaralı liste. Birinci seviye için Arapça numaralandırma (1., 2., 3., ...), ikinci seviye için küçük harfli numaralandırma (a., b., c., ...), üçüncü seviye için küçük harfli Roma numaralandırması (i., ii., iii., ...). Daha sonra biçimlendirme kalan seviyeler için tekrarlanır. |
| NumberArabicDot | `6` | AynısıNumberDefault. |
| NumberArabicParenthesis | `7` | İlk seviyenin numarası "1)"dir. Kalan seviyeler şu şekildedir:NumberDefault. |
| NumberUppercaseRomanDot | `8` | İlk seviyenin numarası "I."dir. Kalan seviyeler de aynıdır.NumberDefault. |
| NumberUppercaseLetterDot | `9` | İlk seviyenin numarası "A."dır. Geri kalan seviyeler de aynıdır.NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | İlk seviyenin numarası "a)"dır. Kalan seviyeler şu şekildedir:NumberDefault. |
| NumberLowercaseLetterDot | `11` | İlk seviyenin numarası "a."dır. Geri kalan seviyeler de aynıdır.NumberDefault. |
| NumberLowercaseRomanDot | `12` | İlk seviyenin numarası "i."dir. Geri kalan seviyeler de aynıdır.NumberDefault. |
| OutlineNumbers | `13` | "1), a), i), (1), (a), (i), 1., a., i." şeklinde numaralandırılmış seviyelere sahip bir taslak liste. |
| OutlineLegal | `14` | Seviyeleri içeren bir taslak liste "1., 1.1., 1.1.1, ..." şeklinde numaralandırılmıştır. |
| OutlineBullets | `15` | Farklı seviyeler için çeşitli maddeler içeren bir taslak liste. |
| OutlineHeadingsArticleSection | `16` | Başlık stillerine bağlı düzeylerin bulunduğu bir ana hat listesi. |
| OutlineHeadingsLegal | `17` | Başlık stillerine bağlı düzeylerin bulunduğu bir ana hat listesi. |
| OutlineHeadingsNumbers | `18` | Başlık stillerine bağlı düzeylerin bulunduğu bir ana hat listesi. |
| OutlineHeadingsChapter | `19` | Başlık stillerine bağlı düzeylerin bulunduğu bir ana hat listesi. |

## Notlar

Bir liste şablonu değeri, the parametresi olarak kullanılır[`Add`](../listcollection/add/) yöntem.

Aspose.Words liste şablonları, Microsoft Word 2003'teki Madde İşaretleri ve Numaralandırma iletişim kutusunda bulunan 21 liste şablonuna karşılık gelir.

## Örnekler

Tüm anahat başlık listesi şablonlarını içeren bir belgenin nasıl oluşturulacağını gösterir.

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

Bir listeyi kopyalayarak listede numaralandırmanın nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve ilk liste düzeyini özelleştirin.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Listemizi bazı paragraflara uygulayalım.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Mevcut bir listenin bir kopyasını belgenin liste koleksiyonuna ekleyebiliriz
// orijinalinde değişiklik yapmadan benzer bir liste oluşturmak.
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

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Aşağıda bir belge oluşturucu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Numaralandırılmış liste:
// Numaralandırılmış listeler, her bir öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// "ListLevelNumber" özelliğini ayarlayarak liste düzeyini artırabiliriz
// geçerli liste öğesinde kendi kendine yeten bir alt liste başlatmak için.
// "NumberDefault" adlı Microsoft Word liste şablonu, ilk liste düzeyi için liste düzeyleri oluşturmak amacıyla sayıları kullanır.
 // Daha derin liste seviyelerinde harfler ve küçük harfli Roma rakamları kullanılır.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Madde işaretli liste:
// Bu liste her paragraftan önce bir girinti ve madde işareti ("•") uygulayacaktır.
// Bu listenin daha derin seviyelerinde "■" ve "○" gibi farklı semboller kullanılacaktır.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// "Liste" bayrağını kaldırarak, sonraki paragrafların liste olarak biçimlendirilmesini önlemek için liste biçimlendirmesini devre dışı bırakabiliriz.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
