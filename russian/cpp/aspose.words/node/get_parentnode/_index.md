---
title: "Метод Aspose::Words::Node::get_ParentNode"
linktitle: "get_ParentNode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Node::get_ParentNode. Получает непосредственного родителя этого узла в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Возвращает непосредственного родителя этого узла.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Примечания


Если узел только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель является **null**.

## Примеры



Показывает, как получить доступ к родительскому узлу узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Добавьте дочерний узел Run в первый абзац документа.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Абзац является родительским узлом узла run. Мы можем проследить эту линию наследования
// до самого узла документа, который является корнем дерева узлов документа.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


Показывает, как создать узел и задать его документ‑владелец.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Мы ещё не добавили этот абзац как дочерний элемент к какому‑либо составному узлу.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Если узел является подходящим типом дочернего узла другого составного узла,
// мы можем присоединить его как дочерний элемент только если оба узла имеют один и тот же документ‑владелец.
// Документ‑владелец — это документ, который мы передали в конструктор узла.
// Мы не присоединили этот абзац к документу, поэтому документ не содержит его текст.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Поскольку документ владеет этим абзацем, мы можем применить один из его стилей к содержимому абзаца.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Добавьте этот узел в документ, а затем проверьте его содержимое.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
