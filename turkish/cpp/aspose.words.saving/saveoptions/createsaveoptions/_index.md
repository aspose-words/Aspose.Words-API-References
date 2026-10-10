---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions method"
linktitle: "CreateSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions yöntemi. Belirtilen kaydetme biçimi için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur C++'da."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Belirtilen kaydetme formatı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kaydetme seçenekleri nesnesinin oluşturulacağı kaydetme biçimi. |

### ReturnValue

[SaveOptions](../) sınıfından türetilen bir sınıfın nesnesi.

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Verilen dosya adında belirtilen dosya uzantısı için uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Bu dosya adının uzantısı, oluşturulacak kaydetme seçenekleri nesnesinin sınıfını belirler. |

### ReturnValue

[SaveOptions](../) sınıfından türetilen bir sınıfın nesnesi.

## Örnekler



Ekli şablonu olmayan belgeler için varsayılan bir şablonun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Otomatik stil güncellemeyi etkinleştirin, ancak bir şablon belgesi eklemeyin.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Şablon belge olmadığı için, belge stil değişikliklerini izlemek için bir yere sahip değildi.
// Bir SaveOptions nesnesi kullanarak şablonu otomatik olarak ayarlayın
// kaydettiğimiz bir belgenin bir şablonu yoksa.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
