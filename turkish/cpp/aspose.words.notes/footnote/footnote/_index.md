---
title: "Aspose::Words::Notes::Footnote::Footnote yapıcı"
linktitle: "Footnote"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::Footnote::Footnote yapıcı. C++'ta Footnote sınıfının bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.notes/footnote/footnote/
---
## Footnote::Footnote constructor


Bir [Footnote](../) sınıfının bir örneğini başlatır.

```cpp
Aspose::Words::Notes::Footnote::Footnote(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Notes::FootnoteType footnoteType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
| footnoteType | Aspose::Words::Notes::FootnoteType | Bu, bir [FootnoteType](../get_footnotetype/) değeri olup, bunun bir dipnot mu yoksa sonnot mu olduğunu belirtir. |
## Açıklamalar


[Footnote](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve [ParentNode](../../../aspose.words/node/get_parentnode/) **null** değerindedir.

Belgeye [Footnote](../) eklemek için, dipnotu eklemek istediğiniz paragrafta [InsertAfter1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) kullanın.

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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
