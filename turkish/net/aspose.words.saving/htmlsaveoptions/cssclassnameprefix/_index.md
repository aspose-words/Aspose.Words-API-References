---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: .NET için Aspose.Words
description: Web tasarımınızın tutarlılığını artırmak için benzersiz bir önekle CSS sınıf adlarını kolayca özelleştirmek için HtmlSaveOptions CssClassNamePrefix özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Tüm CSS sınıf adlarına eklenen bir önek belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıf adlarının ortak bir öneki yoktur.

```csharp
public string CssClassNamePrefix { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Değer boş değil ve geçerli bir CSS tanımlayıcısı değil. |

## Notlar

Bu değer boş değilse, Aspose.Words tarafından oluşturulan tüm CSS sınıfları belirtilen önekle başlar. Bu, örneğin oluşturulan belgelere özel CSS eklerseniz ve class ad çakışmalarını önlemek isterseniz yararlı olabilir.

Eğer değer değilse`hükümsüz` veya boşsa geçerli bir CSS tanımlayıcısı olmalıdır.

## Örnekler

Bir belgenin HTML'ye nasıl kaydedileceğini ve tüm CSS sınıf adlarına bir önek nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
Assert.True(outDocContents.Contains(".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
