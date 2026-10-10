---
title: "Aspose::Words::Saving::HtmlVersion enum"
linktitle: "HtmlVersion"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlVersion enum. Belgenin C++'ta Html ve Mhtml formatlarına kaydedilirken kullanılan HTML sürümünü gösterir."
type: docs
weight: 62000
url: /tr/cpp/aspose.words.saving/htmlversion/
---
## HtmlVersion enum


Belgenin [Html](../../aspose.words/saveformat/) ve [Mhtml](../../aspose.words/saveformat/) formatlarına kaydedilirken kullanılan HTML sürümünü gösterir.

```cpp
enum class HtmlVersion
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Xhtml | 0 | Belgeyi XHTML 1.0 Transitional standardına uygun olarak kaydeder. |
| Html5 | 1 | Belgeyi HTML 5 standardına uygun olarak kaydeder. |


## Örnekler



Bir belgeyi belirli bir HTML sürümüne nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html", options);

// HTML belgelerimiz, farklı HTML sürümleriyle uyumlu olması için küçük farklılıklar içerecektir.
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case Aspose::Words::Saving::HtmlVersion::Html5:
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;

    case Aspose::Words::Saving::HtmlVersion::Xhtml:
        ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;

}
```


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
