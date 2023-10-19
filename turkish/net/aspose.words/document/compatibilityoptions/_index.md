---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: Aspose.Words for .NET
description: Document CompatibilityOptions mülk. Belge uyumluluk seçeneklerine yaniUyumluluk sekmesiSeçenekler Worddeki iletişim kutusu C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

Belge uyumluluk seçeneklerine (yani,**Uyumluluk** sekmesi**Seçenekler** Word'deki iletişim kutusu).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

## Örnekler

Belgenin Microsoft Word'ün farklı sürümleri için nasıl optimize edileceğini gösterir.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Bu nesne, her belgeye özgü kapsamlı bir bayrak listesi içerir
    // bu, Microsoft Word'ün eski sürümleriyle geriye dönük uyumluluğu kolaylaştırmamızı sağlar.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Boş bir belge için varsayılan ayarları yazdırın.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Bu ayarlara Microsoft Word'de "Dosya" -> aracılığıyla erişebiliriz. "Seçenekler" --> "Gelişmiş" -> "Uyumluluk seçenekleri...".
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
/// Bir belgenin uyumluluk seçeneklerindeki tüm bayrakları duruma göre gruplandırır ve ardından her grubu yazdırır.
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

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
