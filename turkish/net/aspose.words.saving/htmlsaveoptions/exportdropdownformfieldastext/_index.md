---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ExportDropDownFormFieldAsText özelliğinin açılır alan biçimlerini kontrol ederek HTML/MHTML dışa aktarımlarınızı nasıl geliştirdiğini keşfedin. Belgelerinizi optimize edin!
type: docs
weight: 130
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Notlar

Ayarlandığında`doğru` , açılır form alanlarını normal metin olarak dışa aktarır. `YANLIŞ`, HTML'de açılır form alanlarını SELECT öğesi olarak dışa aktarır.

EPUB'a aktarırken, metin açılır form alanları bu formatın gereksinimleri nedeniyle her zaman metin olarak kaydedilir.

## Örnekler

HTML'ye kaydederken açılır birleşik kutu form alanlarının paragraf metniyle nasıl harmanlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "İki" değeri seçili olarak bir birleşik kutu eklemek için bir belge oluşturucu kullanın.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Bu SaveOptions nesnesinin "ExportDropDownFormFieldAsText" bayrağı bize şunu sağlar:
// Belgenin HTML'e kaydedilmesinin açılır liste kutularını nasıl ele alacağını kontrol edin.
// "true" olarak ayarlandığında her bir birleşik kutu basit metne dönüştürülecektir
// birleşik kutunun o anda seçili değerini görüntüleyen ve onu etkili bir şekilde donduran.
// "false" olarak ayarlandığında, <select> ve <option> etiketlerini kullanan birleşik kutunun işlevselliği korunacaktır.
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
