---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteType enum. C++'da bunun dipnot mu yoksa sonnot mu olduğunu belirtir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Bunun dipnot mu yoksa sonnot mu olduğunu belirtir.

```cpp
enum class FootnoteType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Footnote | 0 | Nesne bir dipnottur. |
| Sonnot | 1 | Nesne bir sonnottur. |

## Açıklamalar


Hem dipnotlar hem de sonnotlar, [Footnote](./) sınıfı tarafından nesneler olarak temsil edilir. Dipnotlar ve sonnotlar arasında ayrım yapmak için [FootnoteType](../footnote/get_footnotetype/) kullanın.

## Örnekler



Bir dipnot ve bir sonnot ile metne nasıl referans verileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Biraz metin ekleyin ve varsayılan olarak "true" ayarlı IsAuto özelliğine sahip bir dipnot ile işaretleyin,
// böylece gövde metninde görülen işaretçi "1" olarak otomatik numaralandırılacaktır,
// ve dipnot sayfanın alt kısmında görünecektir.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Daha fazla metin ekleyin ve özel bir referans işaretiyle bir sonnot ile işaretleyin,
// bu, "2" numarası yerine kullanılacak ve "IsAuto" özelliği false olarak ayarlanacaktır.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Dipnotlar her zaman referans verilen metnin alt kısmında görünür,
// bu yüzden bu sayfa sonu dipnota etki etmeyecektir.
// Öte yandan, sonnotlar her zaman belgenin sonunda bulunur
// bu sayfa sonu sonnotu bir sonraki sayfaya itecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
