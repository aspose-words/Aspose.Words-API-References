---
title: Class List
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Lists.List sınıf. Bir listenin biçimlendirmesini temsil eder.
type: docs
weight: 3260
url: /tr/net/aspose.words.lists/list/
---
## List class

Bir listenin biçimlendirmesini temsil eder.

```csharp
public class List : IComparable<List>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Sahip belgesini alır. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Bu liste bir liste stili tanımıysa true değerini döndürür. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Bu liste bir liste stiline başvuruysa true değerini döndürür. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Liste 9 düzey içerdiğinde true değerini döndürür; 1 seviye olduğunda yanlış. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer **yanlış** . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Listenin benzersiz tanımlayıcısını alır. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Bu liste için liste düzeylerinin koleksiyonunu alır. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Bu listenin başvurduğu veya tanımladığı liste stilini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(List) | Belirtilen listeyi geçerli listeyle karşılaştırır. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(object) | Belirtilen nesneyi geçerli nesneyle karşılaştırır. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(List) | Belirtilen listeyle karşılaştırır. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(object) |  |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Bu liste nesnesi için karma kodu hesaplar. |

### Notlar

Microsoft Word belgesindeki bir liste, bir liste biçimlendirme özellikleri kümesidir. Her liste en fazla 9 düzeye sahip olabilir ve sayı stili, başlangıç değeri, girintisi, sekme konumu vb. gibi biçimlendirme özellikleri her düzey için ayrı olarak tanımlanır.

A`List` nesne her zaman aittir[`ListCollection`](../listcollection/) Toplamak.

Yeni bir liste oluşturmak için Ekleme yöntemlerini kullanın.[`ListCollection`](../listcollection/) Toplamak.

Bir listenin biçimlendirmesini değiştirmek için şunu kullanın:[`ListLevel`](../listlevel/) içinde bulunan nesneler[`ListLevels`](./listlevels/) Toplamak.

Paragraftan liste biçimlendirmesini uygulamak veya kaldırmak için şunu kullanın:[`ListFormat`](../listformat/).

### Örnekler

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

DocumentBuilder kullanılırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Bir Microsoft Word şablonundan bir liste oluşturun ve liste düzeylerinin ilk ikisini özelleştirin.
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

// Bu NumberFormat değeri, yıldız şeklinde madde işareti listesi sembolleri oluşturacaktır.
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


