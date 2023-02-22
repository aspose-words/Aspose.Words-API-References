---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Açılır form alanlarının HTML veya MHTMLye nasıl kaydedileceğini kontrol eder. Varsayılan değeryanlış .
type: docs
weight: 140
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`yanlış` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

### Notlar

olarak ayarlandığında`doğru` , açılır form alanlarını normal metin olarak dışa aktarır. `yanlış`, açılır form alanlarını HTML'de SELECT öğesi olarak dışa aktarır.

EPUB'a dışa aktarırken, açılır metin form alanları, bu biçimin gereksinimlerine nedeniyle her zaman metin olarak kaydedilir.

### Örnekler

Html'ye kaydederken paragraf metniyle karıştırılacak açılır birleşik kutu form alanlarının nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "İki" değeri seçili bir birleşik giriş kutusu eklemek için bir belge oluşturucu kullanın.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Bu SaveOptions nesnesinin "ExportDropDownFormFieldAsText" bayrağı,
// Belgeyi HTML'ye kaydetmenin açılır birleşik giriş kutularına nasıl davranacağını kontrol edin.
// "true" olarak ayarlamak, her birleşik giriş kutusunu basit metne dönüştürür
// açılan kutunun o anda seçili değerini görüntüleyen, etkin bir şekilde donduran.
// "false" olarak ayarlamak, <select> ve <seçenek> etiketler.
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
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


