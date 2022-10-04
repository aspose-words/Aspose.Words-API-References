---
title: ListCollection
second_title: Aspose.Words for .NET API Referansı
description: Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir.
type: docs
weight: 3270
url: /tr/net/aspose.words.lists/listcollection/
---
## ListCollection class

Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir.

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
| [Add](../../aspose.words.lists/listcollection/add/#add)(ListTemplate) | Önceden tanımlanmış bir şablona dayalı yeni bir liste oluşturur ve bunu belgedeki listeler koleksiyonuna ekler. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(Style) | Bir liste stiline başvuran ve onu belgedeki listeler koleksiyonuna ekleyen yeni bir liste oluşturur. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(List) | Belirtilen listeyi kopyalayıp belgedeki listeler koleksiyonuna ekleyerek yeni bir liste oluşturur. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Belgedeki listeleri numaralandıracak numaralandırıcı nesnesini alır. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(int) | Liste tanımlayıcısına göre bir liste alır. |

### Notlar

Microsoft Word belgesindeki bir liste, bir dizi liste biçimlendirme özelliğidir. Listelerin biçimlendirmesi,[`ListCollection`](./listcollection/) metin paragraflarından ayrı olarak toplama .

Bu sınıfın nesnelerini oluşturmazsınız. her zaman sadece bir tane vardır[`ListCollection`](./listcollection/) Belge başına nesnesi ve şuradan erişilebilir:[`Lists`](../../aspose.words/documentbase/lists/) Emlak.

Önceden tanımlanmış bir liste şablonuna veya bir liste stiline dayalı olarak yeni bir liste oluşturmak için, [`Add`](./add/) yöntem.

Mevcut bir listeyle aynı biçimlendirmeye sahip yeni bir liste oluşturmak için, [`AddCopy`](./addcopy/) yöntem.

Bir paragrafı madde işaretli veya numaralandırılmış yapmak için, bir paragraf atayarak bir paragrafa formatting listesi uygulamanız gerekir.[`List`](../list/) the nesnesi[`List`](../listformat/list/) mülkiyet[`ListFormat`](../listformat/).

Bir paragraftan liste biçimlendirmesini kaldırmak için[`RemoveNumbers`](../listformat/removenumbers/) yöntemi.

WordprocessingML hakkında biraz bilginiz varsa, bunun "liste" ve "liste tanımı" için ayrı concept tanımladığını biliyor olabilirsiniz. Bu tam olarak liste biçimlendirmesinin bir Microsoft Word belgesinde düşük düzeyde nasıl depolandığına karşılık gelir. Liste tanımı bir "şema" gibidir ve listesi, bir liste tanımının bir örneği gibidir.

Programlama modelini basitleştirmek için, Aspose.Words list ve list tanımı arasındaki farkı, Microsoft Word'ün bunu kullanıcı arayüzünde gizlediği gibi gizler. Bu, yerine belgenizin nasıl görünmesini istediğinize daha fazla konsantre olmanızı sağlar. Microsoft Word dosya biçiminin gereksinimlerini karşılamak için düşük düzeyli nesneler oluşturmak.

Aspose.Words. 'nin güncel sürümünde oluşturulduktan sonra listeleri silmek mümkün değildir. Bu, kullanıcının liste tanımları üzerinde açık bir kontrolü olmadığı Microsoft Word'e benzer.

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

* class [List](../list/)
* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
