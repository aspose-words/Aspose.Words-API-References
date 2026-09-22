---
title: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method"
linktitle: "get_IsAtEndOfStructuredDocumentTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag yöntemi. İmleç C++'da bir yapılandırılmış belge etiketinin sonunda ise true döndürür."
type: docs
weight: 19000
url: /tr/cpp/aspose.words/documentbuilder/get_isatendofstructureddocumenttag/
---
## DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method


İmleç yapılandırılmış belge etiketinin sonunda ise **true** döndürür.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag()
```


## Örnekler



[DocumentBuilder](../) imlecini bir yapılandırılmış belge etiketi içinde nasıl hareket ettireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// İmleci hareket ettirmenin birkaç yolu vardır:
// 1 -  Yapısal belge etiketinin ilk karakterine indeksle hareket edin.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Yapısal belge etiketinin ilk karakterine nesneyle hareket edin.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  İkinci yapısal belge etiketinin sonuna hareket edin.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Şu anda seçili olan yapısal belge etiketini alın.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
