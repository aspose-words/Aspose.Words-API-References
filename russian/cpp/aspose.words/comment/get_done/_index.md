---
title: "Метод Aspose::Words::Comment::get_Done"
linktitle: "get_Done"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comment::get_Done. Получает или задает флаг, указывающий, что комментарий помечен как выполненный, в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Получает или задает флаг, указывающий, что комментарий помечен как выполненный.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Примеры



Показывает, как пометить комментарий как "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Вставьте комментарий, чтобы указать на ошибку.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// У комментариев есть флаг "Done", который по умолчанию установлен в "false".
// Если комментарий предлагает внести изменение в документ,
// мы можем применить изменение, а затем также установить флаг "Done", чтобы указать на исправление.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Комментарии, помеченные как "done", будут отличаться
// из тех, которые не "done" с бледным цветом текста.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## См. также

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
