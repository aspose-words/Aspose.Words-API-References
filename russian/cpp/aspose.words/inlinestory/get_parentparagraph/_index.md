---
title: "Aspose::Words::InlineStory::get_ParentParagraph method"
linktitle: "get_ParentParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::InlineStory::get_ParentParagraph method. Получает родительский абзац этого узла в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/inlinestory/get_parentparagraph/
---
## InlineStory::get_ParentParagraph method


Получает родительский [Paragraph](../../paragraph/) этого узла.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::InlineStory::get_ParentParagraph()
```


## Примеры



Показывает, как вставлять узлы [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// У узлов таблицы есть метод "EnsureMinimum()", который гарантирует, что у таблицы есть хотя бы одна ячейка.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Мы можем разместить таблицу внутри сноски, что заставит её отображаться в нижнем колонтитуле страницы, где происходит ссылка.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// У InlineStory также есть метод "EnsureMinimum()", но в этом случае,
// он гарантирует, что последний дочерний элемент узла является абзацем,
// чтобы мы могли легко кликать и вводить текст в Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Отредактируйте внешний вид якоря, который представляет собой маленький верхний индекс
// в основном тексте, указывающий на сноску.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Все узлы inline story имеют свои соответствующие типы историй.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// Комментарий — это другой тип inline story.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// Родительским абзацем встроенного узла истории будет тот, который находится в основном теле документа.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Однако последний абзац — это тот, который берётся из содержимого текста комментария,
// который будет находиться за пределами основного тела документа в речевом пузыре.
// Комментарий по умолчанию не будет иметь дочерних узлов,
// поэтому мы можем применить метод EnsureMinimum() для размещения абзаца здесь также.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Как только у нас появится абзац, мы можем переместить построитель, чтобы выполнить это, и записать наш комментарий.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## См. также

* Class [Paragraph](../../paragraph/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
