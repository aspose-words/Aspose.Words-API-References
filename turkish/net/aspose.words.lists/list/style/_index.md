---
title: List.Style
linktitle: Style
articleTitle: Style
second_title: .NET için Aspose.Words
description: Listelerinizi etkili bir şekilde tanımlamak ve özelleştirmek için Liste Stili özelliğini keşfedin. Benzersiz stil seçenekleriyle web tasarımınızı geliştirin!
type: docs
weight: 80
url: /tr/net/aspose.words.lists/list/style/
---
## List.Style property

Bu listenin başvurduğu veya tanımladığı liste stilini alır.

```csharp
public Style Style { get; }
```

## Notlar

Bu liste bir liste stiliyle ilişkilendirilmemişse, özellik şunu döndürecektir:`hükümsüz`.

Bir liste, bu durumda bir liste stiline referans olabilir[`IsListStyleReference`](../isliststylereference/) olacak`doğru`.

Bu durumda bir liste, bir liste stilinin tanımı olabilir[`IsListStyleDefinition`](../isliststyledefinition/) olacak`doğru`Böyle bir liste doğrudan belgedeki paragraflara uygulanamaz.

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

### Ayrıca bakınız

* class [Style](../../../aspose.words/style/)
* class [List](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
