---
title: List Class
linktitle: List
articleTitle: List
second_title: .NET için Aspose.Words
description: Güçlü liste biçimlendirmesi için Aspose.Words.Lists.List sınıfını keşfedin. Belgelerinizi kusursuz organizasyon ve profesyonel sunumla geliştirin.
type: docs
weight: 3910
url: /tr/net/aspose.words.lists/list/
---
## List class

Bir listenin biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Listelerle Çalışma](https://docs.aspose.com/words/net/working-with-lists/) belgeleme makalesi.

```csharp
public class List : IComparable<List>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Sahip belgesini alır. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Geri Döndürür`doğru` eğer bu liste bir liste stilinin tanımı ise. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Geri Döndürür`doğru` eğer bu liste bir liste stiline referanssa. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Geri Döndürür`doğru` Liste 9 seviyeden oluştuğunda;`YANLIŞ` 1 seviye olduğunda. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer`YANLIŞ` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Listenin benzersiz tanımlayıcısını alır. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Bu liste için liste düzeylerinin koleksiyonunu alır. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Bu listenin başvurduğu veya tanımladığı liste stilini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Belirtilen listeyi geçerli listeyle karşılaştırır. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Belirtilen nesneyi geçerli nesneyle karşılaştırır. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Belirtilen listeyle karşılaştırır. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Bu liste nesnesi için karma kodunu hesaplar. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Mevcut liste ve verilen liste aynı şablondan oluşturulmuşsa doğru değerini döndürür. |

## Notlar

Microsoft Word belgesindeki bir liste, liste biçimlendirme özelliklerinin bir kümesidir. Her liste en fazla 9 düzeye sahip olabilir ve sayı stili, başlangıç değeri, girinti, sekme konumu vb. gibi biçimlendirme özellikleri her düzey için ayrı ayrı tanımlanır.

A`List` nesne her zaman aittir[`ListCollection`](../listcollection/) koleksiyon.

Yeni bir liste oluşturmak için, Add yöntemlerini kullanın[`ListCollection`](../listcollection/) koleksiyon.

Bir listenin biçimlendirmesini değiştirmek için şunu kullanın:[`ListLevel`](../listlevel/) nesneler içinde bulundu[`ListLevels`](./listlevels/) koleksiyon.

Bir paragraftan liste biçimlendirmesini uygulamak veya kaldırmak için şunu kullanın:[`ListFormat`](../listformat/).

## Örnekler

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

DocumentBuilder kullanılırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve liste düzeylerinin ilk ikisini özelleştirin.
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

// Bu NumberFormat değeri yıldız şeklinde madde işaretli liste sembolleri oluşturacaktır.
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
