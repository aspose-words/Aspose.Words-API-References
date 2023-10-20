---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ExportDropDownFormFieldAsText mülk. Açılır form alanlarının HTML veya MHTMLye nasıl kaydedileceğini kontrol eder. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Notlar

olarak ayarlandığında`doğru` , açılır form alanlarını normal metin olarak dışa aktarır. Ne zaman`YANLIŞ`, açılır form alanlarını HTML'deki SELECT öğesi olarak dışa aktarır.

EPUB'a dışa aktarırken, metin açılır form alanları, bu formatın gereklilikleri nedeniyle nedeniyle her zaman metin olarak kaydedilir.

## Örnekler

Html'ye kaydederken açılır açılan kutu form alanlarının paragraf metniyle nasıl harmanlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "İki" değerinin seçili olduğu bir birleşik giriş kutusu eklemek için bir belge oluşturucu kullanın.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Bu SaveOptions nesnesinin "ExportDropDownFormFieldAsText" bayrağı şunları yapmamızı sağlar:
// belgenin HTML'ye kaydedilmesinin açılır açılan kutulara nasıl uygulanacağını kontrol edin.
// Bunu "true" olarak ayarlamak her açılan kutuyu basit metne dönüştürecektir
// açılan kutunun o anda seçili olan değerini görüntüleyerek onu etkili bir şekilde dondurur.
// Bunu "yanlış" olarak ayarlamak, <select> kullanarak açılan kutunun işlevselliğini koruyacaktır. ve <seçenek> Etiketler.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
