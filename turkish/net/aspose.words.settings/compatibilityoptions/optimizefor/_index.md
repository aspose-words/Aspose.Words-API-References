---
title: CompatibilityOptions.OptimizeFor
linktitle: OptimizeFor
articleTitle: OptimizeFor
second_title: Aspose.Words for .NET
description: CompatibilityOptions OptimizeFor yöntem. Belge içeriklerinin yanı sıra varsayılan Aspose.Words davranışının MS Wordün belirli bir sürümüne göre optimize edilmesine olanak tanır C#'da.
type: docs
weight: 720
url: /tr/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Belge içeriklerinin yanı sıra varsayılan Aspose.Words davranışının MS Word'ün belirli bir sürümüne göre optimize edilmesine olanak tanır.

Belge yüklenirken MS Word'ün "Uyumluluk modu" şeridini görüntülemesini önlemek için bu yöntemi kullanın. (Ayrıca[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) özelliğiIso29500_2008_Transitional veya daha yüksek.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

## Örnekler

Bir metin kutusunun metin içeriğinin dikey olarak nasıl hizalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// "VerticalAnchor" özelliğini "TextBoxAnchor.Top" olarak ayarlayın
// bu metin kutusundaki metni şeklin üst tarafıyla hizalayın.
// "VerticalAnchor" özelliğini "TextBoxAnchor.Middle" olarak ayarlayın
// bu metin kutusundaki metni şeklin merkezine hizalayın.
// "VerticalAnchor" özelliğini "TextBoxAnchor.Bottom" olarak ayarlayın
// bu metin kutusundaki metni şeklin alt kısmına hizalayın.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Metin kutularının içindeki metnin dikey hizalanması Microsoft Word 2007'den itibaren mümkündür.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Kaydedilen bir belge için uyulması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003'e uyacak şekilde yapılandırırsak,
// bir görüntünün eklenmesi, VML kullanılarak şeklinin tanımlanmasını sağlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // bu nesneyi geçerken kaydettiğimiz herhangi bir belgenin bu standarda uyması gerekecek.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydedilen belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için DML kullanarak şekli tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

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

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
