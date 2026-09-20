---
title: "Aspose::Words::Layout::LayoutEnumerator::get_Current метод"
linktitle: "get_Current"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::LayoutEnumerator::get_Current method. Получает или задает текущую позицию в модели разметки страницы. Это свойство возвращает непрозрачный объект, соответствующий текущей сущности разметки в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.layout/layoutenumerator/get_current/
---
## LayoutEnumerator::get_Current method


Получает или задает текущую позицию в модели разметки страниц. Это свойство возвращает непрозрачный объект, который соответствует текущему объекту разметки.

```cpp
const System::SharedPtr<System::Object> & Aspose::Words::Layout::LayoutEnumerator::get_Current() const
```


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

* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
