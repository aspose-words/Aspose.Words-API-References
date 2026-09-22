---
title: "Aspose::Words::DocumentBuilder::MoveToBookmark yöntemi"
linktitle: "MoveToBookmark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToBookmark yöntemi. İmleci C++'ta bir yer imine taşır."
type: docs
weight: 52000
url: /tr/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


İmleci bir yer imine taşır.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | İmlecin taşınacağı yer iminin adı. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Açıklamalar


İmleci belirtilen adla yer iminin başlangıcının hemen sonrasına taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamazsa **false** döndürülür ve imleç taşınmaz.

Yeni metin eklemek, yer işaretinin mevcut metnini değiştirmez.

Belgedeki bazı yer işaretlerinin form alanlarına atandığını unutmayın. Böyle bir yer işaretine gidip metin eklemek, metni form alanı koduna ekler. Bu, form alanını geçersiz kılmasa da, eklenen metin alan kodunun bir parçası haline geldiği için görünmez.

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
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


İmleci daha yüksek hassasiyetle bir yer imine taşır.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | İmlecin taşınacağı yer iminin adı. |
| isStart | bool | **true** olduğunda, imleci yer işaretinin başlangıcına taşır. **false** olduğunda, imleci yer işaretinin sonuna taşır. |
| isAfter | bool | **true** olduğunda, imleci yer işaretinin başlangıç ya da bitiş konumundan sonra konumlandırır. **false** olduğunda, imleci yer işaretinin başlangıç ya da bitiş konumundan önce konumlandırır. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Açıklamalar


İmleci yer işaretinin başlangıç ya da bitiş konumundan önce ya da sonra bir konuma taşır.

İstenen konum satır içi seviyede değilse, bir sonraki paragrafın başına taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. Yer imi bulunamazsa **false** döndürülür ve imleç taşınmaz.

## Örnekler



Bir DocumentBuilder'ın düğüm ekleme noktası imlecini bir yer işaretine nasıl taşıyacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geçerli bir yer işareti, bir BookmarkStart düğümü, bir BookmarkEnd düğümü ve
// daha sonra bir yerde eşleşen yer işareti adı ve bu düğümler tarafından kapsanan içerik.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Bir DocumentBuilder'ın imlecini bir yer işaretine taşımanın 4 yolu vardır.
// BookmarkStart ve BookmarkEnd düğümleri arasında ise, imleç yer işaretinin içinde olacaktır.
// Bu, builder tarafından eklenen herhangi bir metnin yer işaretinin bir parçası haline geleceği anlamına gelir.
// 1 -  Yer işaretinin dışında, BookmarkStart düğümünün önünde:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  Yer işaretinin içinde, BookmarkStart düğümünden hemen sonra:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  Yer işaretinin içinde, BookmarkEnd düğümünün tam önünde:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Yer işaretinin dışında, BookmarkEnd düğümünden sonra:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
