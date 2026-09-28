---
title: "Aspose::Words::Node::get_Document метод"
linktitle: "get_Document"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Node::get_Document метод. Получает документ, к которому принадлежит этот узел в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/node/get_document/
---
## Node::get_Document method


Возвращает документ, к которому принадлежит этот узел.

```cpp
virtual System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Node::get_Document() const
```

## Примечания


Узел всегда принадлежит документу, даже если он только что создан и ещё не добавлен в дерево, или если он был удалён из дерева.

## Примеры



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

* Class [DocumentBase](../../documentbase/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
