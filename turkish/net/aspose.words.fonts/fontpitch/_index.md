---
title: Enum FontPitch
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.FontPitch Sıralama. Yazı tipi aralığını temsil eder.
type: docs
weight: 2780
url: /tr/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Yazı tipi aralığını temsil eder.

```csharp
public enum FontPitch
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Default | `0` | Bir yazı tipinin aralığı hakkında hiçbir bilgi bulunmadığını belirtir. |
| Fixed | `1` | Bunun sabit genişlikte bir yazı tipi olduğunu belirtir. |
| Variable | `2` | Bunun orantılı genişlikte bir yazı tipi olduğunu belirtir. |

### Notlar

Aralık, yazı tipinin sabit aralıklı mı, orantılı aralıklı mı yoksa varsayılan bir ayara mı dayalı olduğunu gösterir.

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

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


