---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph method"
linktitle: "MoveToParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph yöntemi. İmleci C++'da geçerli bölümdeki bir paragrafa taşır."
type: docs
weight: 59000
url: /tr/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


İmleci geçerli bölümdeki bir paragrafa taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| paragraphIndex | int32_t | Taşınacak paragrafın indeksi. |
| characterIndex | int32_t | Paragraf içindeki karakterin indeksi. Negatif bir değer, konumu paragrafın sonundan saymanızı sağlar. Paragrafın sonuna gitmek için -1 kullanın. |
## Açıklamalar


Gezinti, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına taşıdıysanız, *paragraphIndex* o bölümün o başlığı içindeki paragrafın indeksini belirtir.

*paragraphIndex* 0'a eşit veya daha büyük olduğunda, bölümün başından itibaren bir indeks belirtir; 0 ilk paragraf olur. *paragraphIndex* 0'dan küçük olduğunda, bölümün sonundan itibaren bir indeks belirtir; -1 son paragraf olur.

## Örnekler



Bir builder'ın imleç konumunu belirli bir paragrafın içine nasıl taşıyacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Belgeyi düzenlemek için bir DocumentBuilder oluşturun. Builder'ın imleci,
// ki, belge oluşturma yöntemlerini çağırdığımızda yeni düğümler ekleyeceği noktadır,
// şu anda belgenin başında bulunur.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Bu imleci farklı bir paragrafın önüne taşıdığınızda, imleç o paragrafın önüne yerleştirilir.
builder->MoveToParagraph(2, 0);

// Eklediğimiz herhangi bir yeni içerik o noktada eklenecektir.
builder->Writeln(u"This is a new third paragraph. ");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
