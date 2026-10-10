---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl metodu"
linktitle: "get_LockContentControl"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl metodu. True olarak ayarlandığında, bu özellik C++'ta bir kullanıcının bu SDT'yi silmesini engeller."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_lockcontentcontrol/
---
## IStructuredDocumentTag::get_LockContentControl method


True olarak ayarlandığında, bu özellik kullanıcının bu **SDT**'yi silmesini engeller.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl()=0
```


## Örnekler



Yapılandırılmış belge etiketlerine düzenleme kısıtlamaları uygulamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Düz metin yapılandırılmış belge etiketi ekleyin; bu etiket, kullanıcıyı doldurması için yönlendiren bir metin kutusu gibi davranır.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Kullanıcının bu metin kutusunun içeriğini düzenlemesini engellemek için "LockContents" özelliğini "true" olarak ayarlayın.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Kullanıcının ... yapmasını engellemek için "LockContentControl" özelliğini "true" olarak ayarlayın
// Microsoft Word'de bu yapılandırılmış belge etiketini manuel olarak silmek.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## Ayrıca Bakınız

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
