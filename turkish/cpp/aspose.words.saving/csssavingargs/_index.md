---
title: "Aspose::Words::Saving::CssSavingArgs sınıfı"
linktitle: "CssSavingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::CssSavingArgs sınıfı. CssSaving() olayı için veri sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


[CssSaving()](../icsssavingcallback/csssaving/) olayı için veri sağlar. Daha fazla bilgi için [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) belge makalesini ziyaret edin.

```cpp
class CssSavingArgs : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | CSS bilgisinin kaydedileceği akışı belirtmeye izin verir. |
| [get_Document](./get_document/)() const | Şu anda kaydedilen belge nesnesini alır. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | CSS'nin bir dosyaya aktarılıp HTML belgesine gömülüp gömülmeyeceğini belirtmeye izin verir. Varsayılan **true**'dur. Bu özellik **false** olduğunda, CSS bilgisi bir CSS dosyasına kaydedilmez ve HTML belgesine gömülmez. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Aspose.Words'un CSS bilgisini kaydettikten sonra akışı açık tutup tutmayacağını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/) için ayarlayıcı. |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | CSS'nin bir dosyaya aktarılıp HTML belgesine gömülüp gömülmeyeceğini belirtmeye izin verir. Varsayılan **true**'dur. Bu özellik **false** olduğunda, CSS bilgisi bir CSS dosyasına kaydedilmez ve HTML belgesine gömülmez. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Varsayılan olarak, Aspose.Words bir belgeyi HTML'ye kaydettiğinde, CSS bilgisini satır içi olarak (her öğenin **style** özniteliğinin değeri olarak) kaydeder.

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

CSS'yi akışa kaydetmek için [CssStream](./get_cssstream/) özelliğini kullanın.

CSS'nin bir dosyaya kaydedilmesini ve HTML belgesine gömülmesini engellemek için [IsExportNeeded](./get_isexportneeded/) özelliğini kullanın.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
