---
title: "Метод Aspose::Words::DocumentBuilder::MoveToBookmark"
linktitle: "MoveToBookmark"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::MoveToBookmark. Перемещает курсор к закладке в C++."
type: docs
weight: 52000
url: /ru/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Перемещает курсор к закладке.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки, к которой нужно переместить курсор. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Примечания


Перемещает курсор в позицию сразу после начала закладки с указанным именем.

Сравнение не чувствительно к регистру. Если закладка не найдена, возвращается **false**, и курсор не перемещается.

Вставка нового текста не заменяет существующий текст закладки.

Обратите внимание, что некоторые закладки в документе привязаны к полям формы. Переход к такой закладке и вставка текста туда вставляет текст в код поля формы. Хотя это не делает поле формы недействительным, вставленный текст не будет виден, потому что он становится частью кода поля.

## Примеры



Показывает, как переместить курсор DocumentBuilder к различным узлам в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте действительную закладку, объект, состоящий из узлов, заключённых между узлом начала закладки,
// и узлом конца закладки.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Курсор DocumentBuilder всегда находится перед узлом, который мы последним добавили.
// Если курсор builder находится в конце документа, его текущий узел будет null.
// Предыдущий узел — это узел конца закладки, который мы последним добавили.
// Добавление новых узлов с помощью builder будет присоединять их к последнему узлу.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Если мы хотим отредактировать другую часть документа с помощью builder,
// нам понадобится переместить его курсор к узлу, который мы хотим отредактировать.
builder->MoveToBookmark(u"MyBookmark");

// Перемещение его к закладке переместит его к первому узлу внутри начального и конечного узлов закладки, заключённому фрагменту.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// Мы также можем переместить курсор к отдельному узлу следующим образом.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Мы можем использовать специальные методы для перехода к началу/концу документа.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Перемещает курсор к закладке с большей точностью.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки, к которой нужно переместить курсор. |
| isStart | bool | Когда **true**, перемещает курсор в начало закладки. Когда **false**, перемещает курсор в конец закладки. |
| isAfter | bool | Когда **true**, перемещает курсор после позиции начала или конца закладки. Когда **false**, перемещает курсор перед позицией начала или конца закладки. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Примечания


Перемещает курсор в позицию перед или после начала или конца закладки.

Если требуемая позиция не находится на уровне встроенного текста, перемещает к следующему абзацу.

Сравнение не чувствительно к регистру. Если закладка не найдена, возвращается **false**, и курсор не перемещается.

## Примеры



Показывает, как переместить курсор точки вставки узла DocumentBuilder к закладке.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Корректная закладка состоит из узла BookmarkStart, узла BookmarkEnd с
// соответствующим именем закладки где‑то позже, и содержимым, заключённым между этими узлами.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Существует 4 способа перемещения курсора DocumentBuilder к закладке.
// Если мы находимся между узлами BookmarkStart и BookmarkEnd, курсор будет внутри закладки.
// Это означает, что любой текст, добавленный построителем, станет частью закладки.
// 1 -  Вне закладки, перед узлом BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  Внутри закладки, сразу после узла BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  Внутри закладки, сразу перед узлом BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Вне закладки, после узла BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
