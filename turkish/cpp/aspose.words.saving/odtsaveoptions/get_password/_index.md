---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password method"
linktitle: "get_Password"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password method. C++'ta belgeyi şifrelemek için bir şifre alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


Belgeyi şifrelemek için bir şifre alır veya ayarlar.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## Açıklamalar


Belgeyi şifrelemeden kaydetmek için bu özellik **null** veya boş bir dize olmalıdır.

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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
