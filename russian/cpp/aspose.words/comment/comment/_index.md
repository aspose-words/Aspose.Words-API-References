---
title: "Конструктор Aspose::Words::Comment::Comment"
linktitle: "Comment"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Comment::Comment. Инициализирует новый экземпляр класса Comment на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Инициализирует новый экземпляр класса [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
## Примечания


Когда создаётся [Comment](../), он принадлежит указанному документу, но ещё не является частью документа, и [ParentNode](../../node/get_parentnode/) имеет значение **null**.

Чтобы добавить [Comment](../) в документ, используйте [InsertAfter1()</see> или <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) в абзаце, где вы хотите вставить комментарий.

После создания комментария не забудьте установить его свойства [Author](../get_author/), [Initial](../get_initial/) и [DateTime](../get_datetime/).

## См. также

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Инициализирует новый экземпляр класса [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
| автор | const System::String\& | Имя автора комментария. Не может быть **null**. |
| инициал | const System::String\& | Инициалы автора комментария. Не могут быть **null**. |
| dateTime | System::DateTime | Дата и время комментария. |

## Примеры



Показывает, как добавить комментарий к абзацу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// В Microsoft Word мы можем щёлкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## См. также

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
