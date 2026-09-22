---
title: "Aspose::Words::DocumentBuilder::MoveTo yöntemi"
linktitle: "MoveTo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveTo yöntemi. İmleci C++'ta bir satır içi düğüme veya bir paragrafın sonuna taşır."
type: docs
weight: 51000
url: /tr/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


İmleci bir satır içi düğüme veya bir paragrafın sonuna taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| düğüm | const System::SharedPtr\<Aspose::Words::Node\>\& | Düğüm bir paragraf ya da bir paragrafın doğrudan çocuğu olmalıdır. |
## Açıklamalar


*node* bir satır içi düzeyde düğüm olduğunda, imleç bu düğüme taşınır ve sonraki içerik o düğümün önüne eklenir.

*node* bir [Paragraph](../../paragraph/) olduğunda, imleç paragrafın sonuna taşınır ve sonraki içerik paragraf sonundan hemen önce eklenir.

*node* bir blok düzeyinde düğüm ancak bir [Paragraph](../../paragraph/) değilse, imleç blok düzeyindeki düğümdeki ilk paragrafın sonuna taşınır ve sonraki içerik paragraf sonundan hemen önce eklenir.

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


Bir [DocumentBuilder](../)'ın imleç konumunu belirli bir düğüme nasıl taşıyacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Belge oluşturucunun bir imleci vardır; bu imleç belgenin bir bölümü gibi davranır
// yapıcı, belge oluşturma yöntemlerini kullandığımızda yeni düğümler ekler.
// Bu imleç, Microsoft Word'ün yanıp sönen imleci gibi aynı şekilde çalışır,
// ve ayrıca, yapıcı tarafından yeni eklenen herhangi bir düğümün hemen sonuna da her zaman yerleşir.
// Belgenin farklı bir bölümüne içerik eklemek için,
// imleci "MoveTo" yöntemiyle başka bir düğüme taşıyabiliriz.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// İmleç artık taşındığı düğümün önündedir.
// İkinci bir run eklemek, onu ilk run'un önüne ekleyecektir.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// İmleci belgenin sonuna taşıyarak, daha önceki gibi metni sona eklemeye devam edebilirsiniz.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
