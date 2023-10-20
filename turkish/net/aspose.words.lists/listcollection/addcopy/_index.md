---
title: ListCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words for .NET
description: ListCollection AddCopy yöntem. Belirtilen listeyi kopyalayıp belgedeki listeler koleksiyonuna ekleyerek yeni bir liste oluşturur C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Belirtilen listeyi kopyalayıp belgedeki listeler koleksiyonuna ekleyerek yeni bir liste oluşturur.

```csharp
public List AddCopy(List srcList)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcList | List | Kopyalanacak kaynak listesi. |

### Geri dönüş değeri

Yeni oluşturulan liste.

## Notlar

Kaynak listesi herhangi bir belgeden olabilir. Kaynak liste farklı bir belgeye aitse, listenin bir kopyası oluşturularak mevcut belgeye eklenir.

Kaynak liste bir liste stiline referans veya tanım ise, yeni oluşturulan liste orijinal liste stiliyle ilişkili değildir.

## Örnekler

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

### Ayrıca bakınız

* class [List](../../list/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
