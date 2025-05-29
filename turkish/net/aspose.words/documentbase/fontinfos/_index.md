---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: .NET için Aspose.Words
description: DocumentBase'in FontInfos özelliğiyle ayrıntılı yazı tipi özelliklerine erişin, belgenizin tasarımını ve okunabilirliğini zahmetsizce geliştirin.
type: docs
weight: 30
url: /tr/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Notlar

Bu yazı tipi tanımları koleksiyonu olduğu gibi belgeden yüklenir. Bazı belgelerde yazı tipi tanımları isteğe bağlı, eksik veya tamamlanmamış olabilir.

Belgede belirli bir yazı tipinin kullanıldığını tespit etmek için bu koleksiyona güvenmeyin. Bu koleksiyonu yalnızca belgede kullanılabilecek yazı tipleri hakkında bilgi edinmek için kullanmalısınız.

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
