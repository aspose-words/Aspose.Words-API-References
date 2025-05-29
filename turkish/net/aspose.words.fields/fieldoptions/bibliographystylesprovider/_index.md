---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: .NET için Aspose.Words
description: Özelleştirilebilir bibliyografya stilleri için FieldOptions BibliographyStylesProvider özelliğini keşfedin ve FieldBibliography ve FieldCitation alanlarınızı geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

x000d_ için bir bibliyografya stili döndüren bir sağlayıcı alır veya ayarlar.[`FieldBibliography`](../../fieldbibliography/) Ve[`FieldCitation`](../../fieldcitation/) alanlar.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Örnekler

Yerleşik stilleri nasıl geçersiz kılacağınızı veya özel bir stil nasıl sağlayacağınızı gösterir.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Eğer belgenin zaten bir stili varsa, aşağıdaki kodla bunu değiştirebilirsiniz:
    // doc.Bibliography.BibliographyStyle = "Bibliyografi özel stili.xsl";

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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
