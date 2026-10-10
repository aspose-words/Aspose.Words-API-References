---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText yöntemi"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText yöntemi. Açılır form alanlarının HTML veya MHTML'ye nasıl kaydedildiğini kontrol eder. Varsayılan değer C++'da false'tur."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Açılır menü form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Açıklamalar


**true** olarak ayarlandığında, açılır form alanlarını normal metin olarak dışa aktarır. **false** olarak ayarlandığında, açılır form alanlarını HTML'de SELECT öğesi olarak dışa aktarır.

EPUB'a dışa aktarırken, metin açılır form alanları bu formatın gereksinimleri nedeniyle her zaman metin olarak kaydedilir.

## Örnekler



HTML'ye kaydederken açılır kombinasyon kutusu form alanlarının paragraf metniyle nasıl bütünleşeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Seçili değeri "Two" olan bir kombinasyon kutusu eklemek için bir belge oluşturucu kullanın.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// Bu SaveOptions nesnesinin "ExportDropDownFormFieldAsText" bayrağı bize şunu yapma imkanı verir
// belgenin HTML'ye kaydedilmesinin açılır kombinasyon kutularını nasıl ele alacağını kontrol eder.
// "true" olarak ayarlamak, her bir kombinasyon kutusunu basit metne dönüştürecektir
// bu, kombinasyon kutusunun şu anda seçili değerini gösterir ve etkili bir şekilde dondurur.
// "false" olarak ayarlamak, kombinasyon kutusunun işlevselliğini <select> ve <option> etiketleri kullanarak koruyacaktır.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
