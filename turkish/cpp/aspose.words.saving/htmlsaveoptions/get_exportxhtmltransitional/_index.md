---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional method"
linktitle: "get_ExportXhtmlTransitional"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional yöntemi. HTML veya MHTML olarak kaydederken DOCTYPE bildirimini yazıp yazmayacağını belirtir. **true** olduğunda, kök öğeden önce belgeye bir DOCTYPE bildirimi yazar. Varsayılan değer **false**'tur. EPUB veya HTML5 (Html5) olarak kaydedildiğinde DOCTYPE bildirimi her zaman C++'da yazılır."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


HTML veya MHTML olarak kaydederken DOCTYPE bildirimini yazıp yazmayacağını belirtir. **true** olduğunda, kök öğeden önce belgeye bir DOCTYPE bildirimi yazar. Varsayılan değer **false**'tur. EPUB veya HTML5 ([Html5](../../htmlversion/)) olarak kaydedildiğinde DOCTYPE bildirimi her zaman yazılır.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Açıklamalar


Aspose.Words bu ayara bakılmaksızın her zaman düzgün biçimlendirilmiş HTML yazar.

**true** olduğunda, HTML çıktı belgesinin başlangıcı şu şekilde görünecektir:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words, XHTML 1.0 Transitional spesifikasyonuna göre XHTML üretmeyi hedefler, ancak çıktı her zaman DTD'ye göre doğrulanmayabilir. Microsoft Word belgesindeki bazı yapılar, XHTML şemasına göre doğrulanacak bir belgeye eşlenmesi zor veya imkansızdır. Örneğin, XHTML iç içe listelere izin vermez (UL başka bir UL öğesi içinde olamaz), ancak Microsoft Word belgelerinde çok seviyeli listeler sıkça görülür.

## Örnekler



Belgeleri Xhtml 1.0 transitional standardına dönüştürürken bir DOCTYPE başlığının nasıl görüntüleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Belgemiz yalnızca "ExportXhtmlTransitional" bayrağını "true" olarak ayarladıysak bir DOCTYPE deklarasyon başlığı içerir.
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
