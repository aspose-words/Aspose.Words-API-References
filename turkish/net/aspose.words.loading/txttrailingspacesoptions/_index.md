---
title: TxtTrailingSpacesOptions Enum
linktitle: TxtTrailingSpacesOptions
articleTitle: TxtTrailingSpacesOptions
second_title: .NET için Aspose.Words
description: Metin dosyalarını içe aktarırken verimli son boşluk yönetimi için Aspose.Words.TxtTrailingSpacesOptions enum'unu keşfedin. Belge işlemenizi bugün geliştirin!
type: docs
weight: 4200
url: /tr/net/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enumeration

İçeri aktarma sırasında son boşlukların işlenmesi için kullanılabilir seçenekleri belirtirText dosya.

```csharp
public enum TxtTrailingSpacesOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Trim | `0` | Sondaki boşluklar kırpılır. |
| Preserve | `1` | Sondaki boşluklar korunur. |

## Örnekler

Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Bir belgenin oluşturucusuna geçirebileceğimiz bir "TxtLoadOptions" nesnesi oluşturun
// düz metin belgenin nasıl yükleneceğini değiştirmek için.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// "LeadingSpacesOptions" özelliğini "TxtLeadingSpacesOptions.Preserve" olarak ayarlayın
// her satırın başındaki tüm boşluk karakterlerini korumak için.
// "LeadingSpacesOptions" özelliğini "TxtLeadingSpacesOptions.ConvertToIndent" olarak ayarlayın
// her satırın başlangıcından tüm boşluk karakterlerini kaldırmak için,
// ve sonra paragrafın ilk satırına sol girinti uygulayarak boşlukların etkisini simüle edin.
// "LeadingSpacesOptions" özelliğini "TxtLeadingSpacesOptions.Trim" olarak ayarlayın
// her satırın başlangıcından tüm boşluk karakterlerini kaldırmak için.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// "TrailingSpacesOptions" özelliğini "TxtTrailingSpacesOptions.Preserve" olarak ayarlayın
 // her satırın sonundaki tüm boşluk karakterlerini korumak için.
 // "TrailingSpacesOptions" özelliğini "TxtTrailingSpacesOptions.Trim" olarak ayarlayın
// her satırın sonundaki tüm boşluk karakterlerini kaldır.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
