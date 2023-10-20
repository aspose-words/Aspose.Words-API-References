---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.FontInfoCollection sınıf. Bir belgede kullanılan yazı tiplerinin bir koleksiyonunu temsil eder C#'da.
type: docs
weight: 2930
url: /tr/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Bir belgede kullanılan yazı tiplerinin bir koleksiyonunu temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Belge kaydedildiğinde TrueType yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Belirtilen ada sahip bir yazı tipini alır. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Katıştırılmış TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Koleksiyonun verilen adda bir yazı tipi içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |

## Notlar

Öğeler[`FontInfo`](../fontinfo/) nesneler.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Kullan[`FontInfos`](../../aspose.words/documentbase/fontinfos/) belgede tanımlanan yazı tiplerinin koleksiyonuna erişim özelliği.

## Örnekler

Bir belgede hangi yazı tiplerinin mevcut olduğuna ilişkin ayrıntıların nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılan ve kullanılmayan yazı tiplerini yazdırın.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

Gömülü TrueType yazı tiplerine sahip bir belgenin nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Ayrıca bakınız

* class [FontInfo](../fontinfo/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
