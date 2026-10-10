---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate yöntemi"
linktitle: "get_DefaultTemplate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate yöntemi. Varsayılan şablonun (dosya adı dahil) yolunu alır veya ayarlar. Bu özelliğin varsayılan değeri C++'da boş bir dizedir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Varsayılan şablona (dosya adı dahil) yolu alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**'dir.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


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
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
