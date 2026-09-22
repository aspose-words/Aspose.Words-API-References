---
title: "Aspose::Words::DocumentBuilder::MoveToDocumentEnd yöntemi"
linktitle: "MoveToDocumentEnd"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToDocumentEnd yöntemi. İmleci C++'ta belgenin sonuna taşır."
type: docs
weight: 54000
url: /tr/cpp/aspose.words/documentbuilder/movetodocumentend/
---
## DocumentBuilder::MoveToDocumentEnd method


İmleci belgenin sonuna taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToDocumentEnd()
```


## Örnekler



Bir document builder'ın imlecini bir belgede farklı düğümlere nasıl taşıyacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geçerli bir yer imi oluşturun; bu, bir yer imi başlangıç düğümüyle çevrili düğümlerden oluşan bir varlıktır,
// ve bir yer imi bitiş düğümü.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Document builder'ın imleci, onunla en son eklediğimiz düğümün her zaman önündedir.
// Eğer builder'ın imleci belgenin sonunda ise, mevcut düğümü null olacaktır.
// Önceki düğüm, en son eklediğimiz yer imi bitiş düğümüdür.
// Builder ile yeni düğümler eklemek, onları son düğüme ekleyecektir.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Builder ile belgenin farklı bir bölümünü düzenlemek istiyorsak,
// imleci düzenlemek istediğimiz düğüme getirmemiz gerekecek.
builder->MoveToBookmark(u"MyBookmark");

// Bir yer imine taşımak, imleci yer imi başlangıç ve bitiş düğümleri arasındaki ilk düğüme, kapsanan çalışmaya taşıyacaktır.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// İmleci bireysel bir düğüme şu şekilde de taşıyabiliriz.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Bir belgenin başlangıç/bitimine taşımak için belirli yöntemleri kullanabiliriz.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
