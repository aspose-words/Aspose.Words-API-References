---
title: List.IsMultiLevel
linktitle: IsMultiLevel
articleTitle: IsMultiLevel
second_title: Aspose.Words for .NET
description: List IsMultiLevel mülk. İadelerdoğru liste 9 düzey içerdiğindeYANLIŞ 1 seviye olduğunda C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

İadeler`doğru` liste 9 düzey içerdiğinde;`YANLIŞ` 1 seviye olduğunda.

```csharp
public bool IsMultiLevel { get; }
```

## Notlar

Aspose.Words ile oluşturduğunuz listeler her zaman çok seviyeli listelerdir ve 9 seviye içerirler.

Microsoft Word 2003 ve sonraki sürümleri her zaman 9 düzeyli çok düzeyli listeler oluşturur. Ancak, Microsoft Word'ün önceki sürümleriyle oluşturulan bazı belgelerde yalnızca 1 düzeyi olan listelerle karşılaşabilirsiniz.

## Örnekler

Liste stilinin nasıl oluşturulacağını ve belgede nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Bir stilin içinde bir List nesnesinin tamamını içerebiliriz.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Listemizdeki tüm liste seviyelerinin görünümünü değiştirin.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Stil içindeki listeden başka bir liste oluşturun.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Listemizin biçimlendireceği bazı liste öğelerini ekleyin.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Liste stiline göre başka bir liste oluşturup uygulayın.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Ayrıca bakınız

* class [List](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
