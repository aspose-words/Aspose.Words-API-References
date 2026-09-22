---
title: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method"
linktitle: "InsertStructuredDocumentTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method. StructuredDocumentTag'i C++'ta belgeye ekler."
type: docs
weight: 46500
url: /tr/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Belgeye bir [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) ekler.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

Bu [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) düğümü yeni eklendi.

## Örnekler



Yapılandırılmış belge etiketini basitçe nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Not, yalnızca aşağıdaki StructuredDocumentTag türlerinin eklenmesine izin verildiğini unutmayın:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Eklenecek StructuredDocumentTag'in işaretleme seviyesi otomatik olarak algılanacak ve eklendiği konuma bağlıdır.
// Eklenen StructuredDocumentTag, imleç konumundan paragraf ve yazı tipi biçimlendirmesini miras alacaktır.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
