---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words for .NET
description: Aspose.Words.Lists.ListLevel sınıf. Liste düzeyi için biçimlendirmeyi tanımlar C#'da.
type: docs
weight: 3500
url: /tr/net/aspose.words.lists/listlevel/
---
## ListLevel class

Liste düzeyi için biçimlendirmeyi tanımlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Listelerle Çalışmak](https://docs.aspose.com/words/net/working-with-lists/) dokümantasyon makalesi.

```csharp
public class ListLevel
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Liste öğesinin gerçek sayısının gerekçesini alır veya ayarlar. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | Bu liste düzeyi için özel sayı stili biçimini alır. Örneğin: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Liste etiketi için kullanılan karakter formatını belirtir. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Geçerli liste düzeyi için resim madde işareti şeklinin görüntü verilerini döndürür. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Düzey devralınan tüm sayıları Arapçaya çeviriyorsa doğru, sayı stilini koruyorsa yanlış. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Bu liste düzeyine bağlı paragraf stilini alır veya ayarlar. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Liste düzeyi için sayı biçimini döndürür veya ayarlar. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Liste düzeyi için sayının veya madde işaretinin konumunu (nokta cinsinden) döndürür veya ayarlar. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Bu liste düzeyi için sayı stilini döndürür veya ayarlar. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Belirtilen liste düzeyi numaralandırmayı yeniden başlatmadan önce görünmesi gereken liste düzeyini ayarlar veya döndürür. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Bu liste düzeyi için başlangıç numarasını döndürür veya ayarlar. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Liste düzeyi için sekme konumunu (nokta cinsinden) döndürür veya ayarlar. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Liste düzeyi için metni kaydırmanın ikinci satırının konumunu (nokta cinsinden) döndürür veya ayarlar. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Liste düzeyi için sayıdan sonra eklenen karakteri döndürür veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Geçerli liste düzeyi için resim madde işareti şeklini oluşturur. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Geçerli liste düzeyine ilişkin resim madde işaretini siler. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Belirtilen ListLevel. ile karşılaştırır |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Bu nesnenin karma kodunu hesaplar. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Dizi gösterimini bildirir.`ListLevel`liste öğesinin belirtilen index nesnesi. Parametreler şunları belirtir:[`NumberStyle`](../../aspose.words/numberstyle/) ve aşağıdaki durumlarda kullanılan isteğe bağlı bir format string Custom belirtildi. |

## Notlar

Bu sınıfın nesnelerini yaratmazsınız. Liste düzeyindeki nesneler, bir liste oluşturulduğunda otomatik olarak oluşturulur. Erişiyorsun`ListLevel` the aracılığıyla nesneler[`ListLevelCollection`](../listlevelcollection/) Toplamak.

Özelliklerini kullanın`ListLevel` ayrı liste düzeyleri için liste biçimlendirmesi 'yi belirtmek için.

## Örnekler

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
