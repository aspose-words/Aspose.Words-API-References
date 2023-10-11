---
title: FieldOptions.BibliographyStylesProvider
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. için kaynakça stili döndüren bir sağlayıcıyı alır veya ayarlar.FieldBibliography VeFieldCitation alanlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

için kaynakça stili döndüren bir sağlayıcıyı alır veya ayarlar.[`FieldBibliography`](../../fieldbibliography/) Ve[`FieldCitation`](../../fieldcitation/) alanlar.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

### Örnekler

Yerleşik stillerin nasıl geçersiz kılınacağını veya özel bir stilin nasıl sağlanacağını gösterir.

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");
}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### Ayrıca bakınız

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


