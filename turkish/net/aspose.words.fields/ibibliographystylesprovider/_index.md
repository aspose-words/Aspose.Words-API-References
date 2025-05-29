---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: .NET için Aspose.Words
description: Atıflarda bibliyografya stillerini özelleştirmek için mükemmel olan Aspose.Words.IBibliographyStylesProvider arayüzüyle belge biçimlendirmenizi geliştirin.
type: docs
weight: 3080
url: /tr/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Bu arayüzü, için bibliyografya stili sağlamak üzere uygulayın[`FieldBibliography`](../fieldbibliography/) Ve[`FieldCitation`](../fieldcitation/) alanlar güncellendiğinde.

```csharp
public interface IBibliographyStylesProvider
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Kaynakça stilini döndürür. |

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
