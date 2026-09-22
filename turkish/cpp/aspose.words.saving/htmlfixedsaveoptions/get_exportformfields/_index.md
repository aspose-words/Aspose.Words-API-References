---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields yöntemi"
linktitle: "get_ExportFormFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields yöntemi. C++'ta form alanlarının etkileşimli öğeler (''input'' etiketi) olarak dışa aktarılıp aktarılmayacağını gösteren değeri alır veya ayarlar, metin veya grafiklere dönüştürülmek yerine."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Form alanlarının metin veya grafik olarak dönüştürülmek yerine etkileşimli öğeler ('input' etiketi) olarak dışa aktarılıp aktarılmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Örnekler



Form alanlarının Html'ye nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// Form alanları içeren bir belgeyi .html'ye dışa aktardığımızda,
// Aspose.Words'un form alanlarını dışa aktarabileceği iki yol vardır.
// "ExportFormFields" bayrağını "true" olarak ayarlamak, onları etkileşimli nesneler olarak dışa aktarır.
// Bu bayrağı "false" olarak ayarlamak, form alanlarını düz metin olarak gösterir.
// Bu, onları mevcut değerlerinde dondurur ve HTML belgemizin okuyucusunun
// onlarla etkileşime girmesini engeller.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
