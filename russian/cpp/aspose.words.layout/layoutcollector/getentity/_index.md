---
title: "Aspose::Words::Layout::LayoutCollector::GetEntity метод"
linktitle: "GetEntity"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::LayoutCollector::GetEntity метод. Возвращает непрозрачную позицию LayoutEnumerator, соответствующую указанному узлу. Вы можете использовать возвращённое значение в качестве аргумента для Current, если перечисляемый документ и документ узла одинаковы в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Возвращает непрозрачную позицию [LayoutEnumerator](../../layoutenumerator/), соответствующую указанному узлу. Вы можете использовать возвращённое значение в качестве аргумента для [Current](../../layoutenumerator/get_current/), если перечисляемый документ и документ узла одинаковы.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Примечания


Этот метод работает только с узлами [Paragraph](../../../aspose.words/paragraph/), а также с неделимыми встроенными узлами, например [BookmarkStart](../../../aspose.words/bookmarkstart/) или [Shape](../../../aspose.words.drawing/shape/). Он не работает с узлами [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) или [Table](../../../aspose.words.tables/table/), а также с узлами в заголовке/нижнем колонтитуле.

Обратите внимание, что сущность, возвращаемая для узла [Paragraph](../../../aspose.words/paragraph/), представляет собой спан разрыва абзаца. Используйте соответствующий метод для перехода к родительской строке.

Если вам нужно перейти к [Run](../../../aspose.words/run/) текста, вы можете вставить закладку непосредственно перед ним и затем перейти к этой закладке.

Если вам нужно перейти к узлу [Cell](../../../aspose.words.tables/cell/), вы можете переместиться к узлу [Paragraph](../../../aspose.words/paragraph/) в этой ячейке, а затем подняться к родительской сущности. Такой же подход можно использовать для узлов [Row](../../../aspose.words.tables/row/) и [Table](../../../aspose.words.tables/table/).

## Примеры



Показывает, как просмотреть диапазоны страниц, охватываемые узлом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Вызовите метод \"GetNumPagesSpanned\", чтобы подсчитать, сколько страниц охватывает содержимое нашего документа.
// Поскольку документ пуст, количество страниц в данный момент равно нулю.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Заполните документ содержимым на 5 страниц.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Перед использованием сборщика макета нам необходимо вызвать метод \"UpdatePageLayout\", чтобы получить
// точную цифру для любой метрики, связанной с макетом, например, количество страниц.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Мы можем увидеть номера начальной и конечной страниц любого узла и их общие диапазоны страниц.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// Мы можем перебрать элементы макета, используя LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// Этот LayoutEnumerator может обходить коллекцию элементов макета как дерево.
// Мы также можем применить его к соответствующему элементу макета любого узла.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## См. также

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
