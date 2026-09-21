---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection-klass"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection-klass. En samling strängar som representerar XML-scheman som är associerade med en anpassad XML-del. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


En samling strängar som representerar XML‑scheman som är associerade med en anpassad XML‑del. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::String\&) | Lägger till ett objekt i samlingen. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [Clone](./clone/)() | Skapar en djup klon av detta objekt. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar eller anger elementet på det angivna indexet. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Hämtar eller anger elementet på det angivna indexet. |
| [IndexOf](./indexof/)(const System::String\&) | Returnerar det nollbaserade indexet för det angivna värdet i samlingen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort det angivna värdet från samlingen. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort ett värde på det angivna indexet. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Anmärkningar


Du skapar inte instanser av den här klassen. Du får åtkomst till samlingen av XML-scheman för en anpassad XML-del via egenskapen [Schemas](../customxmlpart/get_schemas/).

## Exempel



Visar hur man arbetar med en XML-schema-samling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Lägg till en XML-schemaassociation.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Klona den anpassade XML-delens XML-schema-associationssamling,
// och lägg sedan till ett par nya scheman i klonen.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Iterera igenom schemana och skriv ut varje element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Nedan följer tre sätt att ta bort scheman från samlingen.
// 1 -  Ta bort ett schema efter index:
schemas->RemoveAt(2);

// 2 -  Ta bort ett schema efter värde:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Använd metoden "Clear" för att tömma samlingen på en gång.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
