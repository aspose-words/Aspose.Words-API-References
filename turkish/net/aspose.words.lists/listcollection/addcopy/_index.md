---
title: ListCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: .NET için Aspose.Words
description: Bir listeyi zahmetsizce çoğaltmak ve belgenizin koleksiyonunu kolay ve etkili bir şekilde geliştirmek için ListCollection AddCopy yöntemini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Belirtilen listeyi kopyalayıp belgedeki liste koleksiyonuna ekleyerek yeni bir liste oluşturur.

```csharp
public List AddCopy(List srcList)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcList | List | Kopyalanacak kaynak listesi. |

### Geri dönüş değeri

Yeni oluşturulan liste.

## Notlar

Kaynak listesi herhangi bir belgeden olabilir. Kaynak listesi farklı bir belgeye aitse, listenin bir kopyası oluşturulur ve geçerli belgeye eklenir.

Kaynak liste bir liste stilinin referansı veya tanımı ise, yeni oluşturulan liste orijinal liste stiliyle ilişkili değildir.

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

### Ayrıca bakınız

* class [List](../../list/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
