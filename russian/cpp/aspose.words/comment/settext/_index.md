---
title: "Метод Aspose::Words::Comment::SetText"
linktitle: "SetText"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comment::SetText. Это удобный метод, который позволяет легко задавать текст комментария в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Это удобный метод, позволяющий легко задать текст комментария.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| текст | const System::String\& | Новый текст комментария. |
## Примечания


Этот метод позволяет быстро установить текст комментария из строки. Строка может содержать разрывы абзацев, что создаст соответствующие абзацы текста в комментарии. Если вы хотите вставить более сложные элементы в комментарий, например закладки или таблицы или применить богатое форматирование, то необходимо использовать соответствующие классы узлов для построения текста комментария.

## Примеры



Показывает, как добавить комментарий в документ и затем ответить на него.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Разместите комментарий в узле тела документа.
// Этот комментарий будет отображаться в месте своего абзаца,
// вне правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Добавьте ответ, который будет отображаться под родительским комментарием.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Комментарии и ответы являются узлами типа Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Комментарии, которые не являются ответами на другие комментарии, являются "верхнего уровня". У них нет предшествующих комментариев.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Ответы имеют предшествующий комментарий верхнего уровня.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## См. также

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
