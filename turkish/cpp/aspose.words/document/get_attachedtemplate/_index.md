---
title: "Aspose::Words::Document::get_AttachedTemplate metodu"
linktitle: "get_AttachedTemplate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_AttachedTemplate metodu. C++'ta belgeye ekli şablonun tam yolunu alır veya ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Belgeye ekli şablonun tam yolunu alır veya ayarlar.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Açıklamalar


Boş dize, belgenin Normal şablonuna eklendiği anlamına gelir.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
