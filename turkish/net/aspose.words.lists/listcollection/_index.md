---
title: Class ListCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Lists.ListCollection sınıf. Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini saklar ve yönetir.
type: docs
weight: 3470
url: /tr/net/aspose.words.lists/listcollection/
---
## ListCollection class

Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini saklar ve yönetir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Listelerle Çalışmak](https://docs.aspose.com/words/net/working-with-lists/) dokümantasyon makalesi.

```csharp
public class ListCollection : IEnumerable<List>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Belgedeki numaralı ve madde işaretli listelerin sayısını alır. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Sahip belgesini alır. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Dizine göre bir liste alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(ListTemplate) | Önceden tanımlanmış bir şablonu temel alarak yeni bir liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(Style) | Bir liste stiline başvuran yeni bir liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(List) | Belirtilen listeyi kopyalayıp belgedeki listeler koleksiyonuna ekleyerek yeni bir liste oluşturur. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Belgedeki listeleri numaralandıracak numaralandırıcı nesnesini alır. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(int) | Liste tanımlayıcısına göre bir liste alır. |

### Notlar

Microsoft Word belgesindeki liste, bir dizi liste biçimlendirme özelliğidir. Listelerin biçimlendirmesi,`ListCollection` metin paragraflarından ayrı olarak koleksiyonu.

Bu sınıfın nesnelerini yaratmazsınız. Her zaman yalnızca bir tane vardır`ListCollection` Belge başına nesnesi vardır ve bu nesneye[`Lists`](../../aspose.words/documentbase/lists/) mülk.

Önceden tanımlanmış bir liste şablonunu veya liste stilini temel alan yeni bir liste oluşturmak için şunu kullanın:[`Add`](./add/) yöntem.

Mevcut bir listeyle aynı formatta yeni bir liste oluşturmak için komutunu kullanın.[`AddCopy`](./addcopy/) yöntem.

Bir paragrafı madde işaretli veya numaralandırılmış hale getirmek için, bir paragrafa atayarak formatlama listesini uygulamanız gerekir.[`List`](../list/)the 'ye itiraz[`List`](../listformat/list/) mülkiyet[`ListFormat`](../listformat/).

Bir paragraftan liste formatını kaldırmak için[`RemoveNumbers`](../listformat/removenumbers/) yöntemi.

WordprocessingML hakkında biraz bilginiz varsa, "liste" ve "liste tanımı" için ayrı kavramlar tanımladığını biliyor olabilirsiniz. Bu tam olarak bir Microsoft Word belgesinde liste formatının düşük düzeyde nasıl depolandığına (x000d_) karşılık gelir. Liste tanımı bir "şema" gibidir ve listesi, liste tanımının bir örneği gibidir.

Programlama modelini basitleştirmek için Aspose.Words, list ve list tanımı arasındaki ayrımı, Microsoft Word'ün kullanıcı arayüzünde gizlediği gibi gizler. Bu, yerine belgenizin nasıl görünmesini istediğinize daha fazla odaklanmanızı sağlar. Microsoft Word dosya formatının gereksinimlerini karşılamak için düşük seviyeli nesneler oluşturmak.

Aspose.Words'ün mevcut sürümünde listeler oluşturulduktan sonra listeleri silmek mümkün değildir. Bu, kullanıcının liste tanımları üzerinde açık bir kontrole sahip olmadığı Microsoft Word'e benzer.

### Örnekler

Başka bir belgedeki tüm listelerin bir örneğini içeren bir belgenin nasıl oluşturulacağını gösterir.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

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

* class [List](../list/)
* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)


