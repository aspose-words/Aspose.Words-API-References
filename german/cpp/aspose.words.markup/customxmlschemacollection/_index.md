---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection Klasse"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection Klasse. Eine Sammlung von Zeichenketten, die XML‑Schemata darstellen, die mit einem benutzerdefinierten XML‑Teil verknüpft sind. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


Eine Sammlung von Zeichenketten, die XML‑Schemata darstellen, die einem benutzerdefinierten XML‑Teil zugeordnet sind. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&) | Fügt ein Element zur Sammlung hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Clone](./clone/)() | Erstellt eine tiefe Kopie dieses Objekts. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liefert oder setzt das Element am angegebenen Index. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Liefert oder setzt das Element am angegebenen Index. |
| [IndexOf](./indexof/)(const System::String\&) | Gibt den nullbasierten Index des angegebenen Wertes in der Sammlung zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt den angegebenen Wert aus der Sammlung. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt einen Wert am angegebenen Index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Hinweise


Sie erstellen keine Instanzen dieser Klasse. Sie greifen über die Eigenschaft [Schemas](../customxmlpart/get_schemas/) auf die Sammlung von XML‑Schemata eines benutzerdefinierten XML‑Teils zu.

## Beispiele



Zeigt, wie man mit einer XML‑Schemata‑Sammlung arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Fügen Sie eine XML-Schemazuordnung hinzu.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Klonen Sie die XML‑Schema‑Zuordnungs‑Sammlung des benutzerdefinierten XML‑Teils,
// und fügen Sie dann ein paar neue Schemata zum Klon hinzu.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Durchlaufen Sie die Schemata und geben Sie jedes Element aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Im Folgenden werden drei Methoden zum Entfernen von Schemata aus der Sammlung gezeigt.
// 1 - Entfernen Sie ein Schema nach Index:
schemas->RemoveAt(2);

// 2 - Entfernen Sie ein Schema nach Wert:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 - Verwenden Sie die Methode "Clear", um die Sammlung auf einmal zu leeren.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
