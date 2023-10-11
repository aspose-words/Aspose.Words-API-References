---
title: Class ListFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Lists.ListFormat sınıf. Bir paragrafa hangi liste formatının uygulandığını kontrol etmeye izin verir.
type: docs
weight: 3480
url: /tr/net/aspose.words.lists/listformat/
---
## ListFormat class

Bir paragrafa hangi liste formatının uygulandığını kontrol etmeye izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Listelerle Çalışmak](https://docs.aspose.com/words/net/working-with-lists/) dokümantasyon makalesi.

```csharp
public class ListFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Paragrafa madde işaretli veya numaralı biçimlendirme uygulandığında doğrudur. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Bu paragrafın üyesi olduğu listeyi alır veya ayarlar. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Liste düzeyindeki biçimlendirmeyi ve geçerli paragrafa uygulanan biçimlendirme geçersiz kılmalarını döndürür. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Paragrafın liste düzeyi numarasını (0 ila 8) alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Yeni bir varsayılan madde işaretli liste başlatır ve bunu paragrafa uygular. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Yeni bir varsayılan numaralandırılmış liste başlatır ve bunu paragrafa uygular. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Geçerli paragrafın liste düzeyini bir düzey artırır. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Geçerli paragrafın liste düzeyini bir düzey azaltır. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Geçerli paragraftaki sayıları veya madde işaretlerini kaldırır ve liste düzeyini sıfıra ayarlar. |

### Notlar

Bir Microsoft Word belgesindeki bir paragraf madde işaretli veya numaralandırılmış olabilir. Bir paragraf madde işaretli veya numaralandırılmış olduğunda, paragrafa liste biçimlendirme uygulandığı söylenir.

Şunun nesnelerini yaratmıyorsunuz:`ListFormat` doğrudan sınıf. Siz erişin`ListFormat` can 'nin kendisiyle ilişkilendirilmiş liste formatına sahip olduğu başka bir nesnenin özelliği olarak. Şu anda can 'nin liste formatına sahip olduğu nesneler şunlardır:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) Ve[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` bir[`Paragraph`](../../aspose.words/paragraph/) söz konusu paragrafa hangi liste formatının ve liste düzeyinin uygulandığını belirtir .

`ListFormat` bir[`Style`](../../aspose.words/style/) (applicable yalnızca paragraf stillerine) hangi liste formatının ve liste düzeyi 'nin söz konusu stilin tüm paragraflarına uygulandığını belirlemeye olanak tanır.

`ListFormat` bir[`DocumentBuilder`](../../aspose.words/documentbuilder/) , geçerli imleç pozisyonundaki içindeki liste formatına erişim sağlar.[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Liste formatının kendisi bir dosyanın içinde saklanır.[`List`](../list/) Paragraflardan ayrı olarak depolanan nesnesi. liste nesneleri bir içinde saklanır[`ListCollection`](../listcollection/) Toplamak. Bir single var[`ListCollection`](../listcollection/) başına tahsilat[`Document`](../../aspose.words/document/).

Paragraflar fiziksel olarak bir listeye ait değildir. Just paragrafları belirli bir liste nesnesine referans verir.[`List`](./list/) property ve listedeki belirli bir düzey[`ListLevelNumber`](./listlevelnumber/) property. Bu iki özelliği ayarlayarak, bir paragrafa hangi madde işaretlerinin ve numaralandırmanın uygulandığını kontrol edersiniz.

### Örnekler

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


