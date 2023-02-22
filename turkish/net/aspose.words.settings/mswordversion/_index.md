---
title: Enum MsWordVersion
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.MsWordVersion Sıralama. Aspose.Wodsun MS Word sürümüne özel uygulama davranışını taklit etmesine izin verir.
type: docs
weight: 5560
url: /tr/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Aspose.Wods'un MS Word sürümüne özel uygulama davranışını taklit etmesine izin verir.

```csharp
public enum MsWordVersion
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Word2000 | `0` | Aspose.Words davranışını MS Word 2000 sürümüne uyacak şekilde optimize edin. |
| Word2002 | `1` | Aspose.Words davranışını MS Word 2002 sürümüyle eşleşecek şekilde optimize edin. |
| Word2003 | `2` | Aspose.Words davranışını MS Word 2003 sürümüne uyacak şekilde optimize edin. |
| Word2007 | `3` | Aspose.Words davranışını MS Word 2007 sürümüne uyacak şekilde optimize edin. |
| Word2010 | `4` | Aspose.Words davranışını MS Word 2010 sürümüne uyacak şekilde optimize edin. |
| Word2013 | `5` | Aspose.Words davranışını MS Word 2013 sürümüne uyacak şekilde optimize edin. |
| Word2016 | `6` | Aspose.Words davranışını MS Word 2016 sürümüne uyacak şekilde optimize edin. |
| Word2019 | `7` | Aspose.Words davranışını MS Word 2019 sürümüne uyacak şekilde optimize edin. |

### Örnekler

Belgenin farklı Microsoft Word sürümleri için nasıl optimize edileceğini gösterir.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Bu nesne, her belgeye özgü geniş bir bayrak listesi içerir
    // Microsoft Word'ün eski sürümleriyle geriye dönük uyumluluğu kolaylaştırmamızı sağlar.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Boş bir belge için varsayılan ayarları yazdırın.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Bu ayarlara Microsoft Word'de "Dosya" -> "Seçenekler" -> "Gelişmiş" -> "Uyumluluk seçenekleri...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Belirli bir Microsoft Word sürümüyle optimum uyumluluğu sağlamak için OptimizeFor yöntemini kullanabiliriz.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Bir belgenin uyumluluk seçenekleri nesnesindeki tüm bayrakları duruma göre gruplandırır, ardından her grubu yazdırır.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


