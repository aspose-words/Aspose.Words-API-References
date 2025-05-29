---
title: List.IsListStyleDefinition
linktitle: IsListStyleDefinition
articleTitle: IsListStyleDefinition
second_title: .NET için Aspose.Words
description: List IsListStyleDefinition özelliğinin bir liste stilini tanımlayıp tanımlamadığını keşfedin. Listeleriniz için gelişmiş stil seçeneklerinin kilidini bugün açın!
type: docs
weight: 20
url: /tr/net/aspose.words.lists/list/isliststyledefinition/
---
## List.IsListStyleDefinition property

Geri Döndürür`doğru` eğer bu liste bir liste stilinin tanımı ise.

```csharp
public bool IsListStyleDefinition { get; }
```

## Notlar

Bu özellik ne zaman`doğru` ,[`Style`](../style/) özellik, bu listenin tanımladığı that liste stilini döndürür.

Bir liste stilini tanımlayan bir listenin özelliklerini değiştirerek, liste stilinin properties özelliğini değiştirirsiniz.

Bir liste stilinin tanımı olan bir liste, paragraphs öğelerine doğrudan uygulanarak numaralandırılamaz.

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

* class [List](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
