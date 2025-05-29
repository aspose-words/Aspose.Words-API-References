---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Sorunsuz kaydetme için Docx, Docm, Dotx, Dotm veya FlatOpc gibi belge biçimlerini kolayca seçmek amacıyla OoxmlSaveOptions' SaveFormat özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Docx ,Docm , Dotx ,Dotm veyaFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Kaydedilen bir belgenin uyması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003 ile uyumlu olacak şekilde yapılandırırsak,
// Bir resim eklemek, VML kullanılarak şeklinin tanımlanmasını sağlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // Bu nesneyi geçirirken kaydettiğimiz her belgenin o standarda uyması gerekecektir.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydedilen belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için şekli DML kullanarak tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
