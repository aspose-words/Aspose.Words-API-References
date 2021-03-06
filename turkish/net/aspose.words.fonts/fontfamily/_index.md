---
title: FontFamily
second_title: Aspose.Words for .NET API Referansı
description: Yazı tipi ailesini temsil eder.
type: docs
weight: 2730
url: /tr/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Yazı tipi ailesini temsil eder.

```csharp
public enum FontFamily
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Genel bir aile adı belirtir. Bu ad, yazı tipi hakkında bilgi olmadığında veya önemli olmadığında kullanılır. Varsayılan yazı tipi kullanılır. |
| Roman | `1` | Seriflerle orantılı bir yazı tipi belirtir. Bir örnek Times New Roman. |
| Swiss | `2` | Serif içermeyen orantılı bir yazı tipi belirtir. Bir örnek Arial. |
| Modern | `3` | Serif içeren veya içermeyen tek aralıklı bir yazı tipi belirtir. Tek aralıklı yazı tipleri genellikle moderndir; örnekler Pica, Elite ve Courier New'i içerir. |
| Script | `4` | El yazısı gibi görünecek şekilde tasarlanmış bir yazı tipini belirtir; örnekler arasında Script ve Cursive. bulunur |
| Decorative | `5` | Yeni bir yazı tipi belirtir. Bir örnek Eski İngilizcedir. |

### Notlar

Yazı tipi ailesi, ortak çizgi genişliğine ve serif özelliklerine sahip bir yazı tipi grubudur.

### Örnekler

Bir belgedeki her yazı tipinin ayrıntılarına nasıl erişileceğini ve yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Alt adlar genellikle boştur.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
