---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: .NET için Aspose.Words
description: Madde işaretli ve numaralı listelerin etkili yönetimi, belge biçimlendirmesinin ve organizasyonunun iyileştirilmesi için Aspose.Words.Lists.ListCollection sınıfını keşfedin.
type: docs
weight: 3920
url: /tr/net/aspose.words.lists/listcollection/
---
## ListCollection class

Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Listelerle Çalışma](https://docs.aspose.com/words/net/working-with-lists/) belgeleme makalesi.

```csharp
public class ListCollection : IEnumerable<List>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Belgedeki numaralı ve madde işaretli listelerin sayısını alır. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Sahip belgesini alır. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Dizin numarasına göre bir liste alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | Önceden tanımlanmış bir şablona dayalı yeni bir liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | Bir liste stiline başvuran yeni bir liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | Belirtilen listeyi kopyalayıp belgedeki liste koleksiyonuna ekleyerek yeni bir liste oluşturur. |
| [AddSingleLevelList](../../aspose.words.lists/listcollection/addsinglelevellist/)(*[ListTemplate](../listtemplate/)*) | Önceden tanımlanmış şablona dayalı yeni bir tek düzeyli liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Belgedeki listeleri numaralandıracak numaratör nesnesini alır. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | Bir liste tanımlayıcısına göre bir liste alır. |

## Notlar

Microsoft Word belgesindeki bir liste, bir dizi liste biçimlendirme özelliğidir. Listelerin biçimlendirmesi,`ListCollection` Metin paragraflarından ayrı ayrı koleksiyonu.

Bu sınıftan nesneler oluşturmazsınız. Her zaman yalnızca bir tane vardır`ListCollection` Belge başına nesnesi ve bu nesneye şu şekilde erişilebilir:[`Lists`](../../aspose.words/documentbase/lists/) mülk.

Önceden tanımlanmış bir liste şablonuna veya bir liste stiline dayalı yeni bir liste oluşturmak için, öğesini kullanın[`Add`](./add/) yöntem.

Mevcut bir listeyle aynı biçimlendirmeye sahip yeni bir liste oluşturmak için, öğesini kullanın[`AddCopy`](./addcopy/) yöntem.

Bir paragrafı madde işaretli veya numaralı yapmak için, paragrafa bir liste biçimlendirme atayarak uygulamanız gerekir.[`List`](../list/)the 'ye nesne[`List`](../listformat/list/) mülkiyeti[`ListFormat`](../listformat/).

Bir paragraftan liste biçimlendirmesini kaldırmak için şunu kullanın:[`RemoveNumbers`](../listformat/removenumbers/) yöntemi.

WordprocessingML hakkında biraz bilginiz varsa, "liste" ve "liste tanımı" için ayrı kavramlar tanımladığını biliyor olabilirsiniz. Bu, tam olarak liste biçimlendirmesinin düşük seviyedeki bir Microsoft Word belgesinde nasıl saklandığına karşılık gelir. Liste tanımı bir "şema" gibidir ve liste bir liste tanımı örneği gibidir.

Programlama modelini basitleştirmek için Aspose.Words, Microsoft Word'ün kullanıcı arayüzünde gizlediği gibi, liste ve liste tanımı arasındaki ayrımı gizler. Bu, Microsoft Word dosya biçiminin gereksinimlerini karşılamak için düşük seviyeli nesneler oluşturmak yerine, belgenizin nasıl görünmesini istediğinize daha fazla konsantre olmanızı sağlar.

Aspose.Words. 'nin güncel sürümünde listeler oluşturulduktan sonra silinemez. Bu, kullanıcının liste tanımları üzerinde açık bir kontrole sahip olmadığı Microsoft Word'e benzerdir.

## Örnekler

Başka bir belgedeki tüm listelerin örneklerini içeren bir belgenin nasıl oluşturulacağını gösterir.

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

* class [List](../list/)
* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
