---
title: "Aspose::Words::MailMerging::MappedDataFieldCollection Klasse"
linktitle: "MappedDataFieldCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MappedDataFieldCollection Klasse. Ermöglicht das automatische Zuordnen zwischen Feldnamen in Ihrer Datenquelle und Seriendruckfeldnamen im Dokument. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Ermöglicht das automatische Zuordnen zwischen Feldnamen in Ihrer Datenquelle und den Namen der Seriendruckfelder im Dokument. Weitere Informationen finden Sie im Dokumentationsartikel [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Fügt eine neue Feldzuordnung hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [ContainsKey](./containskey/)(const System::String\&) | Bestimmt, ob eine Zuordnung des angegebenen Feldes im Dokument in der Sammlung vorhanden ist. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Bestimmt, ob eine Zuordnung des angegebenen Feldes in der Datenquelle in der Sammlung vorhanden ist. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Wörterbuch‑Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Liest oder setzt den Namen des Feldes in der Datenquelle, das dem angegebenen Seriendruckfeld zugeordnet ist. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Liest oder setzt den Namen des Feldes in der Datenquelle, das dem angegebenen Seriendruckfeld zugeordnet ist. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt eine Feldzuordnung. |
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


Dies ist als Sammlung von Zeichenketten-Schlüsseln zu Zeichenketten-Werten implementiert. Die Schlüssel sind die Namen der Seriendruckfelder im Dokument und die Werte sind die Namen der Felder in Ihrer Datenquelle.

## Siehe auch

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
