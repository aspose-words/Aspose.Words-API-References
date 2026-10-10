---
title: "Aspose::Words::DocumentBuilder::InsertFootnote yöntemi"
linktitle: "InsertFootnote"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertFootnote yöntemi. Belgeye bir dipnot veya sonnot ekler C++'ta."
type: docs
weight: 35000
url: /tr/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Belgeye bir dipnot veya sonnot ekler.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Bir dipnot mu yoksa sonnot mu ekleneceğini belirtir. |
| footnoteText | const System::String\& | Dipnotun metnini belirtir. |

### ReturnValue

Yeni oluşturulan bir dipnot nesnesini döndürür.

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

## Ayrıca Bakınız

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Belgeye bir dipnot veya sonnot ekler.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Bir dipnot mu yoksa sonnot mu ekleneceğini belirtir. |
| footnoteText | const System::String\& | Dipnotun metnini belirtir. |
| referenceMark | const System::String\& | Dipnotun özel referans işaretini belirtir. |

### ReturnValue

Yeni oluşturulan bir dipnot nesnesini döndürür.

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

## Ayrıca Bakınız

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
