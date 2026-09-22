---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag method"
linktitle: "MoveToStructuredDocumentTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag yöntemi. İmleci C++'ta yapılandırılmış belge etiketine taşır."
type: docs
weight: 61000
url: /tr/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


İmleci yapılandırılmış belge etiketine taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\\<Aspose::Words::Markup::StructuredDocumentTag\\>\\& | Taşınacak yapılandırılmış belge etiketi. |
| characterIndex | int32_t | Yapılandırılmış belge etiketi içindeki karakterin indeksi. Negatif bir değer, etiketin sonundan bir konum belirtmenizi sağlar. -1 kullanarak etiketin sonuna hareket edin. Etiket blok seviyesinde ise ve imleci son paragrafının sonuna taşımak istiyorsanız, -2 belirtin. |

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

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


İmleci geçerli bölümdeki bir yapılandırılmış belge etiketine taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | Hareket edilecek yapısal belge etiketinin indeksi. |
| characterIndex | int32_t | Yapılandırılmış belge etiketi içindeki karakterin indeksi. Negatif bir değer, etiketin sonundan bir konum belirtmenizi sağlar. -1 kullanarak etiketin sonuna hareket edin. Etiket blok seviyesinde ise ve imleci son paragrafının sonuna taşımak istiyorsanız, -2 belirtin. |
## Açıklamalar


Gezinti, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına taşıdıysanız, *structuredDocumentTagIndex* o başlık içindeki yapısal belge etiketinin indeksini belirtir.

*structuredDocumentTagIndex* 0'a eşit veya büyük olduğunda, bölümün başından bir indeks belirtir; 0 ilk yapısal belge etiketi olur. *structuredDocumentTagIndex* 0'dan küçük olduğunda, bölümün sonundan bir indeks belirtir; -1 son yapısal belge etiketi olur.

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
