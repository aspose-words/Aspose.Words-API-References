---
title: "Aspose::Words::Markup::SmartTag::SmartTag конструктор"
linktitle: "SmartTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::SmartTag::SmartTag конструктор. Инициализирует новый экземпляр класса SmartTag в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Инициализирует новый экземпляр класса [SmartTag](../).

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
## Примечания


Когда вы создаёте новый узел, необходимо указать документ, к которому принадлежит узел. Узел не может существовать без документа, поскольку зависит от структур, общих для документа, таких как списки и стили. Хотя узел всегда принадлежит документу, он может быть частью дерева документа или нет.

Когда узел создаётся, он принадлежит документу, но ещё не является частью дерева документа, и [ParentNode](../../../aspose.words/node/get_parentnode/) имеет значение null. Чтобы вставить узел в документ, используйте методы [InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) у родительского узла.

## См. также

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
