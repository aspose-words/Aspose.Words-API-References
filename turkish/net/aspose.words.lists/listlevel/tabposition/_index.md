---
title: ListLevel.TabPosition
linktitle: TabPosition
articleTitle: TabPosition
second_title: .NET için Aspose.Words
description: Liste düzeyleriniz için sekme konumlarını noktalar halinde kolayca ayarlamak ve belgenizin biçimlendirmesini geliştirmek için ListLevel TabPosition özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.lists/listlevel/tabposition/
---
## ListLevel.TabPosition property

Liste düzeyi için sekme konumunu (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double TabPosition { get; set; }
```

## Notlar

Yalnızca şu durumlarda etkilidir:[`TrailingCharacter`](../trailingcharacter/) bir sekmedir.

## Örnekler

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

* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
