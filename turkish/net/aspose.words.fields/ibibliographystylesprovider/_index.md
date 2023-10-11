---
title: Interface IBibliographyStylesProvider
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.IBibliographyStylesProvider arayüz. için kaynakça stili sağlamak üzere bu arayüzü uygulayın FieldBibliography VeFieldCitation güncellendiklerinde alanlar.
type: docs
weight: 2670
url: /tr/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

için kaynakça stili sağlamak üzere bu arayüzü uygulayın [`FieldBibliography`](../fieldbibliography/) Ve[`FieldCitation`](../fieldcitation/) güncellendiklerinde alanlar.

```csharp
public interface IBibliographyStylesProvider
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(string) | Kaynakça stilini döndürür. |

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


