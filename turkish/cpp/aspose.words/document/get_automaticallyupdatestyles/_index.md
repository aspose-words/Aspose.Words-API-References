---
title: "Aspose::Words::Document::get_AutomaticallyUpdateStyles yöntemi"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_AutomaticallyUpdateStyles yöntemi. Belge her MS Word'ta C++ ile açıldığında, ekli şablondaki stillere eşleşecek şekilde belgedeki stillerin güncellenip güncellenmeyeceğini belirten bir bayrağı alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Belge her MS Word'ta açıldığında, belgedeki stillerin ekli şablondaki stillerle eşleşecek şekilde güncellenip güncellenmeyeceğini gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Örnekler



Bir şablonu belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Microsoft Word belgeleri varsayılan olarak "Normal.dotm" adlı bir ekli şablonla birlikte gelir.
// Boş Aspose.Words belgeleri için varsayılan bir şablon yoktur.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Bir şablon ekleyin, ardından stil değişikliklerini uygulamak için bayrağı ayarlayın
// şablon içinde belgemizdeki stillere.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
