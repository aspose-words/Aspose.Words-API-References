---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: .NET için Aspose.Words
description: BibliographyStyle özelliğini keşfedin, bibliyografinizin etkin stilini kolayca yönetin ve özelleştirin; böylece gelişmiş organizasyon ve sunum elde edin.
type: docs
weight: 10
url: /tr/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Bir bibliyografya için kullanılacak etkin stilin adını temsil eden bir dize alır veya ayarlar.

```csharp
public string BibliographyStyle { get; set; }
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

* class [Bibliography](../)
* ad alanı [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* toplantı [Aspose.Words](../../../)
