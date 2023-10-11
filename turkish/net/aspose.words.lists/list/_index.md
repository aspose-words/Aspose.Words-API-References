---
title: Class List
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Lists.List sınıf. Bir listenin biçimlendirmesini temsil eder.
type: docs
weight: 3460
url: /tr/net/aspose.words.lists/list/
---
## List class

Bir listenin biçimlendirmesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Listelerle Çalışmak](https://docs.aspose.com/words/net/working-with-lists/) dokümantasyon makalesi.

```csharp
public class List : IComparable<List>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Sahip belgesini alır. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | İadeler`doğru` bu liste bir liste stilinin tanımıysa. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | İadeler`doğru` bu liste bir liste stiline referans ise. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | İadeler`doğru` liste 9 düzey içerdiğinde;`YANLIŞ` 1 seviye olduğunda. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Listenin benzersiz tanımlayıcısını alır. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Bu liste için liste düzeylerinin koleksiyonunu alır. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Bu listenin başvuruda bulunduğu veya tanımladığı liste stilini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(List) | Belirtilen listeyi geçerli listeyle karşılaştırır. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(object) | Belirtilen nesneyi geçerli nesneyle karşılaştırır. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(List) | Belirtilen listeyle karşılaştırır. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(object) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Bu liste nesnesi için karma kodunu hesaplar. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(List) | Geçerli liste ile verilen liste aynı şablondan oluşturulmuşsa true değerini döndürür. |

### Notlar

Microsoft Word belgesindeki liste, bir dizi liste biçimlendirme özelliğidir. Her listede en fazla 9 düzey bulunabilir ve sayı stili, başlangıç değeri, girinti, sekme konumu vb. gibi biçimlendirme özellikleri her düzey için ayrı ayrı tanımlanır.

A`List` nesne her zaman ona aittir[`ListCollection`](../listcollection/) Toplamak.

Yeni bir liste oluşturmak için Ekle yöntemlerini kullanın.[`ListCollection`](../listcollection/) Toplamak.

Bir listenin biçimlendirmesini değiştirmek için şunu kullanın:[`ListLevel`](../listlevel/) 'de bulunan nesneler[`ListLevels`](./listlevels/) Toplamak.

Bir paragrafa liste biçimlendirmesi uygulamak veya kaldırmak için şunu kullanın:[`ListFormat`](../listformat/).

### Örnekler

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

DocumentBuilder kullanılırken özel liste formatının paragraflara nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve liste seviyelerinin ilk ikisini özelleştirin.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Bu NumberFormat değeri yıldız şekilli madde işareti listesi sembolleri oluşturacaktır.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Paragraflar oluşturun ve özel liste biçimlendirmemizin her iki liste düzeyini de bunlara uygulayın.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
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


