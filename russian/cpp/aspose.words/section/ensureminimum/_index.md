---
title: "Aspose::Words::Section::EnsureMinimum метод"
linktitle: "EnsureMinimum"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Section::EnsureMinimum метод. Обеспечивает наличие у раздела Body с одним Paragraph в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/section/ensureminimum/
---
## Section::EnsureMinimum method


Обеспечивает, что у раздела есть [Body](../get_body/) с одним [Paragraph](../../paragraph/).

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


## Примеры



Показывает, как подготовить новый узел раздела для редактирования.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит раздел, у которого есть тело, которое, в свою очередь, имеет абзац.
// Мы можем добавить содержимое в этот документ, добавляя такие элементы, как текстовые фрагменты, фигуры или таблицы, в этот абзац.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Если мы добавим новый раздел таким образом, у него не будет тела или каких-либо других дочерних узлов.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Выполните метод "EnsureMinimum", чтобы добавить тело и абзац в этот раздел и начать его редактирование.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
