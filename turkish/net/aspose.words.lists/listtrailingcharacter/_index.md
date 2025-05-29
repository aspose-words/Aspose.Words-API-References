---
title: ListTrailingCharacter Enum
linktitle: ListTrailingCharacter
articleTitle: ListTrailingCharacter
second_title: .NET için Aspose.Words
description: Liste etiketlerini özelleştirmek ve paragraf biçimlendirmesini geliştirerek kusursuz bir belge sunumu için Aspose.Words.Lists.ListTrailingCharacter enum'unu keşfedin.
type: docs
weight: 3990
url: /tr/net/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enumeration

Liste etiketini paragrafın metninden ayıran karakteri belirtir.

```csharp
public enum ListTrailingCharacter
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Tab | `0` | Liste etiketi ile paragraf metni arasına bir sekme karakteri yerleştirilir. |
| Space | `1` | Liste etiketi ile paragraf metni arasına bir boşluk karakteri yerleştirilir. |
| Nothing | `2` | Liste etiketi ile paragraf metni arasında ayırıcı karakter yoktur. |

## Notlar

Bir değer olarak kullanılır[`TrailingCharacter`](../listlevel/trailingcharacter/) mülk.

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

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
