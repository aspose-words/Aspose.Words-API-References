---
title: ListLevelCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: ListLevelCollection Item özelliğiyle liste düzeylerine zahmetsizce erişin. Sorunsuz belge biçimlendirmesi için herhangi bir düzeyi dizine göre alın.
type: docs
weight: 20
url: /tr/net/aspose.words.lists/listlevelcollection/item/
---
## ListLevelCollection indexer

Dizin düzeyinde bir liste alır.

```csharp
public ListLevel this[int index] { get; set; }
```

## Örnekler

Bir liste stilinin nasıl oluşturulacağını ve bir belgede nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Bir stilin içerisinde bütün bir Liste nesnesini barındırabiliriz.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Listemizdeki tüm liste seviyelerinin görünümünü değiştirelim.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Bir stil içindeki listeden başka bir liste oluştur.
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

// Liste stiline göre başka bir liste oluştur ve uygula.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

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

* class [ListLevel](../../listlevel/)
* class [ListLevelCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
