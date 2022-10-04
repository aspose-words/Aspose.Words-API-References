---
title: ListTemplate
second_title: Aspose.Words for .NET API Referansı
description: Microsoft Wordde bulunan önceden tanımlanmış liste biçimlerinden birini belirtir.
type: docs
weight: 3330
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
| BulletDefault | `0` | seviyeli varsayılan madde işaretli liste. Birinci seviyenin madde işareti bir disktir, ikinci seviyenin madde işareti bir dairedir, üçüncü seviyenin madde işareti bir karedir. Ardından biçimlendirme, kalan seviyeler için tekrarlanır. |
| BulletDisk | `0` | BulletDefault ile aynı. |
| BulletCircle | `1` | İlk seviyenin mermisi bir dairedir. Kalan seviyeler BulletDefault ile aynıdır. |
| BulletSquare | `2` | İlk seviyenin mermisi bir karedir. Kalan seviyeler BulletDefault ile aynıdır. |
| BulletDiamonds | `3` | İlk seviyenin mermisi 4 elmaslı bir Wingding karakteridir. Kalan seviyeler BulletDefault ile aynıdır. |
| BulletArrowHead | `4` | İlk seviyenin mermisi bir ok başı Wingding karakteridir. Kalan seviyeler BulletDefault ile aynıdır. |
| BulletTick | `5` | İlk seviyenin mermisi bir kene Wingding karakteridir. Kalan seviyeler BulletDefault ile aynıdır. |
| NumberDefault | `6` | 9 seviyeli varsayılan numaralı liste. Birinci seviye için Arapça numaralandırma (1., 2., 3., ...), ikinci seviye için küçük harfli numaralandırma (a., b., c., ...), küçük harfli romen numaralandırma (i ., ii., iii., ...) üçüncü seviye için. Ardından biçimlendirme kalan seviyeler için tekrarlanır. |
| NumberArabicDot | `6` | NumberDefault ile aynı. |
| NumberArabicParenthesis | `7` | İlk seviyenin numarası "1)" dir. Kalan düzeyler NumberDefault'dakiyle aynıdır. |
| NumberUppercaseRomanDot | `8` | İlk seviyenin numarası "I" dir. Kalan düzeyler NumberDefault'dakiyle aynıdır. |
| NumberUppercaseLetterDot | `9` | İlk seviyenin numarası "A"dır. Kalan düzeyler NumberDefault'dakiyle aynıdır. |
| NumberLowercaseLetterParenthesis | `10` | İlk seviyenin numarası "a)" dır. Kalan düzeyler NumberDefault'dakiyle aynıdır. |
| NumberLowercaseLetterDot | `11` | İlk seviyenin numarası "a" dır. Kalan düzeyler NumberDefault'dakiyle aynıdır. |
| NumberLowercaseRomanDot | `12` | İlk seviyenin numarası "i" dir. Kalan düzeyler NumberDefault'dakiyle aynıdır. |
| OutlineNumbers | `13` | "1), a), i), (1), (a), (i), 1., a., i." numaralı seviyeleri içeren bir taslak liste. |
| OutlineLegal | `14` | Seviyeleri olan bir anahat listesi "1., 1.1., 1.1.1, ..." olarak numaralandırılmıştır. |
| OutlineBullets | `15` | Farklı seviyeler için çeşitli madde işaretleri içeren bir anahat listeleri. |
| OutlineHeadingsArticleSection | `16` | Başlık stillerine bağlı düzeylere sahip bir anahat listesi. |
| OutlineHeadingsLegal | `17` | Başlık stillerine bağlı düzeylere sahip bir anahat listesi. |
| OutlineHeadingsNumbers | `18` | Başlık stillerine bağlı düzeylere sahip bir anahat listesi. |
| OutlineHeadingsChapter | `19` | Başlık stillerine bağlı düzeylere sahip bir anahat listesi. |

### Notlar

Bir liste şablonu değeri, the içinde parametre olarak kullanılır[`Add`](../listcollection/add/) yöntem.

Aspose.Words liste şablonları, Microsoft Word 2003'te Madde İşaretleri ve Numaralandırma iletişim kutusundaki mevcut 21 liste şablonuna karşılık gelir.

### Örnekler

Tüm anahat başlıkları liste şablonlarını içeren bir belgenin nasıl oluşturulacağını gösterir.

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

Bir listeyi kopyalayarak bir listede numaralandırmanın nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Bir Microsoft Word şablonundan bir liste oluşturun ve ilk liste düzeyini özelleştirin.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Listemizi bazı paragraflara uygula.
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

Liste seviyeleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Aşağıda, bir belge oluşturucu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Numaralandırılmış bir liste:
// Numaralandırılmış listeler, her bir öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// "ListLevelNumber" özelliğini ayarlayarak liste seviyesini yükseltebiliriz
// geçerli liste öğesinde bağımsız bir alt liste başlatmak için.
// "NumberDefault" adlı Microsoft Word liste şablonu, ilk liste düzeyi için liste düzeyleri oluşturmak için sayıları kullanır.
// Daha derin liste seviyelerinde harfler ve küçük Romen rakamları kullanılır. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Madde işaretli bir liste:
// Bu liste, her paragraftan önce bir girinti ve bir madde işareti ("•") uygular.
// Bu listenin daha derin seviyelerinde "■" ve "○" gibi farklı semboller kullanılacaktır.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// "Liste" bayrağının ayarını kaldırarak, sonraki paragrafları liste olarak biçimlendirmemek için liste biçimlendirmesini devre dışı bırakabiliriz.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
