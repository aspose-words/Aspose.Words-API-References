---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary yöntemi"
linktitle: "get_IsTemporary"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary yöntemi. Bu SDT'nin içeriği C++'ta değiştirildiğinde WordProcessingML belgesinden kaldırılıp kaldırılmayacağını belirtir."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Bu **SDT**'nin içeriği değiştirildiğinde WordProcessingML belgesinden kaldırılıp kaldırılmayacağını belirtir.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Örnekler



Tek kullanımlık denetimlerin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Düz metin bir yapılandırılmış belge etiketi ekleyin,
// Bu, kullanıcının metin girebileceği düz metin bir form olarak davranacaktır.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// "IsTemporary" özelliğini "true" olarak ayarlayın ve
// Kullanıcı Microsoft Word'de bir kez düzenledikten sonra içeriğini belgeye dahil eder.
// "IsTemporary" özelliğini "false" olarak ayarlayarak kullanıcının içeriği düzenlemesine izin verin
// yapılandırılmış belge etiketini istediği kadar kez düzenleyebilmesini.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Bir onay kutusu şeklinde başka bir yapılandırılmış belge etiketi ekleyin ve varsayılan durumunu "checked" olarak ayarlayın.
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// "IsTemporary" özelliğini "true" olarak ayarlayarak onay kutusunun bir simgeye dönüşmesini sağlayın
// kullanıcı Microsoft Word'de ona tıkladığında.
// "IsTemporary" özelliğini "false" olarak ayarlayarak kullanıcının onay kutusuna istediği kadar tıklamasına izin verin.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
