---
title: "Aspose::Words::DocumentBuilder::StartBookmark метод"
linktitle: "StartBookmark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::StartBookmark метод. Помечает текущую позицию в документе как начало закладки в C++."
type: docs
weight: 68000
url: /ru/cpp/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder::StartBookmark method


Помечает текущую позицию в документе как начало закладки.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartBookmark(const System::String &bookmarkName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки. |

### ReturnValue

Узел начала закладки, только что созданный.
## Примечания


Закладки в документе могут перекрываться и охватывать любой диапазон. Чтобы создать действительную закладку, необходимо вызвать как [StartBookmark()](../), так и [EndBookmark()](../) с одинаковым параметром *bookmarkName*.

Некорректно сформированные закладки или закладки с дублирующимися именами будут игнорироваться при сохранении документа.

## Примеры



Показывает, как создать закладку.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Действительная закладка должна иметь текст тела документа, заключённый в
// Узлы BookmarkStart и BookmarkEnd, созданные с соответствующим именем закладки.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Показывает, как вставить гиперссылку, ссылающуюся на локальную закладку.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Вставьте поле HYPERLINK, которое ссылается на закладку. Мы можем передать переключатели поля
// в метод "InsertHyperlink" в качестве части аргумента, содержащего имя ссылочной закладки.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## См. также

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
