---
title: "Aspose::Words::Markup::CustomXmlPartCollection class"
linktitle: "CustomXmlPartCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomXmlPartCollection class. Представляет коллекцию пользовательских XML‑частей. Элементы являются объектами CustomXmlPart. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class


Представляет коллекцию пользовательских XML‑частей. Элементы являются объектами [CustomXmlPart](../customxmlpart/). Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Добавляет элемент в коллекцию. |
| [Add](./add/)(const System::String\&, const System::String\&) | Создаёт новую часть XML с указанным XML и добавляет её в коллекцию. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Удаляет все элементы из коллекции. |
| [Clone](./clone/)() | Создаёт глубокую копию этой коллекции и её элементов. |
| [CustomXmlPartCollection](./customxmlpartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetById](./getbyid/)(const System::String\&) | Находит и возвращает пользовательскую часть XML по её идентификатору. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает или задает элемент по указанному индексу. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Получает или задает элемент по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Удаляет элемент по указанному индексу. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Типовое определение | Описание |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Примечания


Обычно вам не нужно создавать экземпляры этого класса. Вы можете получить доступ к пользовательским XML‑данным, хранящимся в документе, через свойство [CustomXmlParts](../../aspose.words/document/get_customxmlparts/).

## Примеры



Показывает, как создать структурированный тег документа с пользовательскими XML-данными.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте XML‑часть, содержащую данные, и добавьте её в коллекцию документа.
// Если включить вкладку "Developer" в Microsoft Word,
// мы можем найти элементы этой коллекции в "XML Mapping Pane", вместе с несколькими элементами по умолчанию.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Ниже представлены два способа обращения к XML‑частям.
// 1 -  По индексу в коллекции пользовательских XML‑частей:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  По GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Добавьте ассоциацию XML‑схемы.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Клонируйте часть, а затем вставьте её в коллекцию.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Итерируйте по коллекции и выводите содержимое каждой части.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Используйте метод "RemoveAt" для удаления клонированной части по индексу.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Клонируйте коллекцию XML‑частей, а затем используйте метод "Clear" для одновременного удаления всех её элементов.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Создайте структурированный тег документа, который будет отображать содержимое нашей части, и вставьте его в тело документа.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## См. также

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
