---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: .NET için Aspose.Words
description: Gelişmiş akademik yazım için bibliyografya stillerini zahmetsizce almak ve özelleştirmek amacıyla IBibliographyStylesProvider GetStyle yöntemini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Kaynakça stilini döndürür.

```csharp
public Stream GetStyle(string styleFileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| styleFileName | String | Bibliyografya stili dosya adı. |

### Geri dönüş değeri

TheStream XSLT stil sayfası bibliyografya stili ile.

## Notlar

Uygulama şunu döndürmelidir:`hükümsüz` belirtilen stilin MS Word sürümünün kullanılması gerektiğini belirtmek için

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

* interface [IBibliographyStylesProvider](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
