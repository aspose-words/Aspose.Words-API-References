---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor"
linktitle: "OdtSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor. Bu sınıfın yeni bir örneğini başlatır ve C++'ta Odt formatında bir belge kaydetmek için kullanılabilir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Odt](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Örnekler



Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Ayrıca Bakınız

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi [Odt](../../../aspose.words/saveformat/) veya [Ott](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Bu, [Odt](../../../aspose.words/saveformat/) veya [Ott](../../../aspose.words/saveformat/) olabilir. |

## Örnekler



Kaydedilmiş bir ODT/OTT belgesini şifreyle nasıl şifreleyip ardından Aspose.Words kullanarak nasıl yükleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Yeni bir OdtSaveOptions oluşturun ve "SaveFormat.Odt" değerlerinden birini geçirin,
// "SaveFormat.Ott" değerini belgeyi kaydetmek için format olarak kullanın.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Bu belgeyi uygun bir düzenleyiciyle açarsak,
// SaveOptions nesnesinde belirttiğimiz şifreyi soracaktır.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Aspose.Words kullanarak bu belgeyi tekrar açmak veya düzenlemek istersek,
// yükleme yapıcı metoduna doğru şifreyi içeren bir LoadOptions nesnesi sağlamamız gerekir.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Bu sınıfın yeni bir örneğini başlatır; bu örnek belgeyi şifreyle korunan [Odt](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## Ayrıca Bakınız

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
