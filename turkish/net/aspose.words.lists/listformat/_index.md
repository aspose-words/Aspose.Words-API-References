---
title: Class ListFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Lists.ListFormat sınıf. Bir paragrafa hangi liste biçimlendirmesinin uygulanacağını kontrol etmeye izin verir.
type: docs
weight: 3280
url: /tr/net/aspose.words.lists/listformat/
---
## ListFormat class

Bir paragrafa hangi liste biçimlendirmesinin uygulanacağını kontrol etmeye izin verir.

```csharp
public class ListFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Paragrafa madde işaretli veya numaralı biçimlendirme uygulandığında doğrudur. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Bu paragrafın üyesi olduğu listeyi alır veya ayarlar. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Liste düzeyinde biçimlendirme artı geçerli paragrafa uygulanan biçimlendirme geçersiz kılma işlemlerini döndürür. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Paragraf için liste düzeyi numarasını (0 ila 8) alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Yeni bir varsayılan madde işaretli liste başlatır ve bunu paragrafa uygular. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Yeni bir varsayılan numaralandırılmış liste başlatır ve bunu paragrafa uygular. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Geçerli paragrafın liste düzeyini bir düzey artırır. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Geçerli paragrafın liste düzeyini bir düzey azaltır. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Geçerli paragraftan sayıları veya madde işaretlerini kaldırır ve liste düzeyini sıfıra ayarlar. |

### Notlar

Microsoft Word belgesindeki bir paragraf madde işaretli veya numaralandırılmış olabilir. Paragraf madde işaretli veya numaralandırılmışsa, paragrafa liste biçimlendirme uygulandığı söylenir.

nesnelerini oluşturmazsınız.`ListFormat` doğrudan sınıf. Siz erişin`ListFormat` can ile ilişkili liste biçimlendirmesine sahip başka bir nesnenin özelliği olarak. Şu anda liste biçimlendirmesine sahip olan can nesneleri şunlardır:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) ve[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` bir[`Paragraph`](../../aspose.words/paragraph/) o paragrafa hangi liste biçimlendirmesinin ve liste düzeyinin uygulanacağını belirtir .

`ListFormat` bir[`Style`](../../aspose.words/style/)(applicable yalnızca paragraf stillerine), o belirli stilin tüm paragraflarına hangi liste biçimlendirmesinin ve list level uygulanacağını belirtmeye olanak tanır.

`ListFormat` bir[`DocumentBuilder`](../../aspose.words/documentbuilder/) , içindeki geçerli imleç konumunda liste biçimlendirmesine erişim sağlar.[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Liste biçimlendirmenin kendisi bir[`List`](../list/) Paragraflardan ayrı olarak depolanan nesnesi. object listesi, bir[`ListCollection`](../listcollection/) Toplamak. tek bir var[`ListCollection`](../listcollection/) başına toplama[`Document`](../../aspose.words/document/).

Paragraflar fiziksel olarak bir listeye ait değildir. just paragrafları, belirli bir liste nesnesine şu şekilde başvurur:[`List`](./list/) property ve listedeki belirli bir seviye aracılığıyla[`ListLevelNumber`](./listlevelnumber/) property. Bu iki özelliği ayarlayarak, bir paragrafa hangi madde işaretlerinin ve numaralandırmanın uygulanacağını kontrol edersiniz.

### Örnekler

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


