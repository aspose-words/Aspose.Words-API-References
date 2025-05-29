---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: .NET için Aspose.Words
description: Belge yazı tiplerini etkili bir şekilde yönetmek ve belgenizin görsel çekiciliğini artırmak için başvuracağınız çözüm olan Aspose.Words.Fonts.FontInfoCollection sınıfını keşfedin.
type: docs
weight: 3360
url: /tr/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Bir belgede kullanılan yazı tiplerinin bir koleksiyonunu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Bir belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Belirtilen ada sahip bir yazı tipi alır. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Gömülü TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Koleksiyonun verilen ada sahip bir yazı tipi içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |

## Notlar

Öğeler şunlardır[`FontInfo`](../fontinfo/) nesneler.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Şunu kullanın:[`FontInfos`](../../aspose.words/documentbase/fontinfos/) Belgede tanımlanan yazı tipleri koleksiyonuna erişmek için özellik.

## Örnekler

TrueType yazı tiplerinin gömülü olduğu bir belgenin nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

Bir belgede hangi yazı tiplerinin bulunduğunun ayrıntılarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılan ve kullanılmayan yazı tiplerini yazdır.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Ayrıca bakınız

* class [FontInfo](../fontinfo/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
