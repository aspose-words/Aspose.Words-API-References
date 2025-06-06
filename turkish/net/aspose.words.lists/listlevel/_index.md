---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: .NET için Aspose.Words
description: Gelişmiş liste biçimlendirme için Aspose.Words.Lists.ListLevel sınıfını keşfedin. Belgenizin yapısını güçlü, özelleştirilebilir seçeneklerle geliştirin.
type: docs
weight: 3950
url: /tr/net/aspose.words.lists/listlevel/
---
## ListLevel class

Bir liste düzeyi için biçimlendirmeyi tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Listelerle Çalışma](https://docs.aspose.com/words/net/working-with-lists/) belgeleme makalesi.

```csharp
public class ListLevel
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Liste öğesinin gerçek sayısının gerekçesini alır veya ayarlar. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; set; } | Bu liste düzeyi için özel sayı stili biçimini alır veya ayarlar. Örneğin: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Liste etiketi için kullanılan karakter biçimlendirmesini belirtir. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Mevcut liste düzeyi için resim madde işareti şeklinin resim verilerini döndürür. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Düzey tüm miras alınan sayıları Arapçaya çevirirse doğru, sayı stillerini korursa yanlış. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Bu liste düzeyine bağlı olan paragraf stilini alır veya ayarlar. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Liste düzeyi için sayı biçimini döndürür veya ayarlar. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Liste düzeyi için sayının veya madde işaretinin konumunu (nokta cinsinden) döndürür veya ayarlar. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Bu liste düzeyi için sayı stilini döndürür veya ayarlar. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Belirtilen liste düzeyi numaralandırmayı yeniden başlatmadan önce görünmesi gereken liste düzeyini ayarlar veya döndürür. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Bu liste düzeyi için başlangıç numarasını döndürür veya ayarlar. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Liste düzeyi için sekme konumunu (nokta cinsinden) döndürür veya ayarlar. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Liste düzeyi için sarma metninin ikinci satırının konumunu (nokta cinsinden) döndürür veya ayarlar. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Liste düzeyi için sayıdan sonra eklenen karakteri döndürür veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Mevcut liste düzeyi için resim madde işareti şekli oluşturur. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Mevcut liste düzeyi için resim madde işaretini siler. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Belirtilen ListLevel ile karşılaştırır. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Bu nesne için karma kodunu hesaplar. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Dize gösterimini bildirir`ListLevel`Liste öğesinin belirtilen index için nesne. Parametreler şunu belirtir:[`NumberStyle`](../../aspose.words/numberstyle/) ve isteğe bağlı bir biçim string kullanıldığındaCustom belirtildi. |

## Notlar

Bu sınıfın nesnelerini oluşturmazsınız. Liste düzeyi nesneleri, bir liste oluşturulduğunda otomatik olarak oluşturulur. Erişiminiz`ListLevel` nesneler the yoluyla[`ListLevelCollection`](../listlevelcollection/) koleksiyon.

Özelliklerini kullanın`ListLevel` bireysel liste düzeyleri için liste biçimlendirmesini belirtmek için.

## Örnekler

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
