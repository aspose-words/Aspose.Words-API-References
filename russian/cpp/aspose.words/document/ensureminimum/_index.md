---
title: "Aspose::Words::Document::EnsureMinimum метод"
linktitle: "EnsureMinimum"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::EnsureMinimum. Если документ не содержит разделов, создает один раздел с одним абзацем в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Если документ не содержит разделов, создаёт один раздел с одним абзацем.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Примеры



Показывает, как гарантировать, что документ содержит минимальный набор узлов, необходимых для редактирования его содержимого.
```cpp
// Новосозданный документ содержит один дочерний Section, который включает один дочерний Body и один дочерний Paragraph.
// Мы можем редактировать содержимое тела документа, добавляя узлы, такие как Runs или встроенные Shapes, в этот абзац.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Это минимальный набор узлов, необходимых для возможности редактировать документ.
// Мы больше не сможем редактировать документ, если удалим любой из них.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Вызовите этот метод, чтобы убедиться, что документ содержит как минимум эти три узла, чтобы мы могли снова его редактировать.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
