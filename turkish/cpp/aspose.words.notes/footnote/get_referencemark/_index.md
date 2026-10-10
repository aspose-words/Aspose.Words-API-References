---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark metodu"
linktitle: "get_ReferenceMark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::Footnote::get_ReferenceMark metodu. Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer **empty string**'dir, bu da C++'ta otomatik numaralı dipnotların kullanıldığı anlamına gelir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer **empty string**'dir, bu da otomatik numaralı dipnotların kullanıldığı anlamına gelir.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## Açıklamalar


Bu özellik **empty string** veya **null** olarak ayarlanırsa, [IsAuto](../get_isauto/) özelliği otomatik olarak **true** değerine ayarlanır; başka bir değere ayarlanırsa [IsAuto](../get_isauto/) **false** olur.

RTF formatı yalnızca 1 sembolü özel referans işareti olarak depolayabilir, bu nedenle dışa aktarımda yalnızca ilk sembol yazılır, diğerleri atılır.

## Örnekler



Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Metin ekleyin ve bir dipnot ile referans verin. Bu dipnot, küçük bir üst simge referansı yerleştirecek
// referans verdiği metnin ardından bir işaret koyacak ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturacaktır.
// Bu giriş, dipnotun referans işaretini ve referans metnini içerecektir,
// bunu belge oluşturucunun "InsertFootnote" metoduna geçireceğiz.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Bu özellik "true" olarak ayarlanırsa, dipnotumuzun referans işareti
// bölümdeki tüm dipnotlar arasında indeksine eşit olacaktır.
// Bu ilk dipnottur, bu yüzden referans işareti "1" olacaktır.
ASSERT_TRUE(footnote->get_IsAuto());

// Belge oluşturucuyu dipnotun içine taşıyarak referans metnini düzenleyebiliriz.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti ayarlayabiliriz.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// "IsAuto" bayrağı true olarak ayarlı bir yer imi hâlâ gerçek indeksini gösterecektir
// önceki yer imleri özel referans işaretleri gösterse bile, bu yer iminin referans işareti "3" olacaktır.
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## Ayrıca Bakınız

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
