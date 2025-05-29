---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: .NET için Aspose.Words
description: Aspose.Words.Lists.ListFormat sınıfıyla belgelerinizde ana liste biçimlendirmesini yapın. Daha iyi okunabilirlik için paragraf stilini zahmetsizce geliştirin.
type: docs
weight: 3930
url: /tr/net/aspose.words.lists/listformat/
---
## ListFormat class

Bir paragrafa hangi liste biçimlendirmesinin uygulanacağını kontrol etmenizi sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Listelerle Çalışma](https://docs.aspose.com/words/net/working-with-lists/) belgeleme makalesi.

```csharp
public class ListFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Paragrafa madde işaretli veya numaralı biçimlendirme uygulandığında doğrudur. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Bu paragrafın üyesi olduğu listeyi alır veya ayarlar. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Liste düzeyi biçimlendirmesini ve geçerli paragrafa uygulanan biçimlendirme geçersiz kılmalarını döndürür. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Paragraf için liste düzeyi numarasını (0 ila 8) alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Yeni bir varsayılan madde işaretli liste başlatır ve bunu paragrafa uygular. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Yeni bir varsayılan numaralandırılmış liste başlatır ve bunu paragrafa uygular. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Mevcut paragrafın liste seviyesini bir seviye artırır. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Geçerli paragrafın liste düzeyini bir düzey azaltır. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Geçerli paragraftan numaraları veya madde işaretlerini kaldırır ve liste düzeyini sıfıra ayarlar. |

## Notlar

Microsoft Word belgesindeki bir paragraf madde işaretli veya numaralı olabilir. Bir paragraf madde işaretli veya numaralı olduğunda, paragrafa liste biçimlendirmesinin uygulandığı söylenir.

Nesneleri yaratmazsınız`ListFormat` sınıfa doğrudan erişin. `ListFormat`can ile ilişkilendirilmiş liste biçimlendirmesine sahip olabilecek başka bir nesnenin özelliği olarak. Şu anda can ile ilişkilendirilmiş liste biçimlendirmesine sahip nesneler şunlardır:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) Ve[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` Birinin[`Paragraph`](../../aspose.words/paragraph/) specifies belirli paragrafa hangi liste biçimlendirmesinin ve liste düzeyinin uygulanacağını belirtir.

`ListFormat` Birinin[`Style`](../../aspose.words/style/) (applicable yalnızca paragraf stilleri için) belirli stildeki tüm paragraflara hangi liste biçimlendirmesinin ve liste level uygulanacağını belirtmenize olanak tanır.

`ListFormat` Birinin[`DocumentBuilder`](../../aspose.words/documentbuilder/) , geçerli imleç konumunda liste biçimlendirmesine erişim sağlar[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Liste biçimlendirmesinin kendisi bir[`List`](../list/) Paragraflardan ayrı olarak depolanan nesnesi. Liste nesneleri bir[`ListCollection`](../listcollection/) koleksiyon. Tek bir var[`ListCollection`](../listcollection/) koleksiyon başına[`Document`](../../aspose.words/document/).

Paragraflar fiziksel olarak bir listeye ait değildir. Paragraflar just belirli bir liste nesnesine şu şekilde başvurur:[`List`](./list/) property ve listedeki belirli bir seviye[`ListLevelNumber`](./listlevelnumber/) property. Bu iki özelliği ayarlayarak bir paragrafa hangi madde işaretlerinin ve numaralandırmanın uygulanacağını kontrol edersiniz.

## Örnekler

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
