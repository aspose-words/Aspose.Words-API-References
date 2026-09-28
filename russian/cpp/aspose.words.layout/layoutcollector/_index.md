---
title: "Класс Aspose::Words::Layout::LayoutCollector"
linktitle: "LayoutCollector"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Layout::LayoutCollector. Этот класс позволяет вычислять номера страниц узлов документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Этот класс позволяет вычислять номера страниц узлов документа. Чтобы узнать больше, посетите статью документации [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Очищает все собранные данные макета. Вызовите этот метод после того, как документ был обновлён вручную или макет был перестроен. |
| [get_Document](./get_document/)() const | Получает или задаёт документ, к которому привязан этот экземпляр сборщика. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает индекс страницы, где заканчивается узел, начиная с 1. Возвращает 0, если узел нельзя сопоставить со страницей. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает непрозрачную позицию [LayoutEnumerator](../layoutenumerator/), соответствующую указанному узлу. Вы можете использовать возвращённое значение в качестве аргумента для [Current](../layoutenumerator/get_current/), при условии, что перечисляемый документ и документ узла одинаковы. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает количество страниц, охватываемых указанным узлом. 0, если узел находится на одной странице. Это то же самое, что [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает индекс страницы, где начинается узел, начиная с 1. Возвращает 0, если узел нельзя сопоставить со страницей. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Инициализирует экземпляр этого класса. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Сеттер для [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Примечания


Когда вы создаёте [LayoutCollector](./) и указываете объект [Document](../../aspose.words/document/) для привязки, сборщик будет фиксировать сопоставление узлов документа с объектами макета при форматировании документа в страницы.

Вы сможете определить, на какой странице находится конкретный узел документа (например, run, абзац или ячейка таблицы), используя методы [GetStartPageIndex()](../), [GetEndPageIndex()](../) и [GetNumPagesSpanned()](../). Эти методы автоматически строят модель макета страниц документа и обновляют поля при необходимости.

Когда сбор информации о макете больше не нужен, лучше установить свойство [Document](./get_document/) в **null**, чтобы избежать ненужного сбора дополнительных сопоставлений макета.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
