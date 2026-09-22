---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::FontSavingArgs sınıfı. FontSaving() olayı için veri sağlar. Daha fazla bilgi edinmek için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


[FontSaving()](../ifontsavingcallback/fontsaving/) olayı için veri sağlar. Daha fazla bilgi edinmek için [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) belge makalesini ziyaret edin.

```cpp
class FontSavingArgs : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Bold](./get_bold/)() const | Geçerli yazı tipinin kalın olup olmadığını gösterir. |
| [get_Document](./get_document/)() const | Kaydedilen belge nesnesini alır. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Geçerli yazı tipi ailesi adını gösterir. |
| [get_FontFileName](./get_fontfilename/)() const | Yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [get_FontStream](./get_fontstream/)() const | Yazı tipinin kaydedileceği akışı belirtmeye olanak tanır. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılıp aktarılmayacağını belirtmeye olanak tanır. Varsayılan **true** değeridir. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılmadan önce alt küme oluşturulup oluşturulmayacağını belirtmeye olanak tanır. |
| [get_Italic](./get_italic/)() const | Geçerli yazı tipinin italik olup olmadığını gösterir. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Aspose.Words'ün akışı açık tutup tutmayacağını veya bir yazı tipi kaydedildikten sonra kapatıp kapatmayacağını belirtir. |
| [get_OriginalFileName](./get_originalfilename/)() const | Orijinal yazı tipi dosya adını uzantısıyla birlikte alır. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Orijinal yazı tipi dosya boyutunu alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Ayarlayıcı: [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılıp aktarılmayacağını belirtmeye olanak tanır. Varsayılan **true** değeridir. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Ayarlayıcı: [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Ayarlayıcı: [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Açıklamalar


Aspose.Words bir belgeyi HTML veya ilgili biçimlere kaydettiğinde ve [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) **true** olarak ayarlandığında, her bir yazı tipi ihracat konusunu ayrı bir dosyaya kaydeder.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Belirli bir yazı tipi kaynağını kaydedip kaydetmeyeceğinize karar vermek için, [IsExportNeeded](./get_isexportneeded/) özelliğini kullanın.

Yazı tiplerini dosyalar yerine akışlara kaydetmek için, [FontStream](./get_fontstream/) özelliğini kullanın.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
