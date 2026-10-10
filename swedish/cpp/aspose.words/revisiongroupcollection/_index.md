---
title: "Aspose::Words::RevisionGroupCollection class"
linktitle: "RevisionGroupCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionGroupCollection class. En samling av RevisionGroup-objekt som representerar revisionsgrupper i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 55000
url: /sv/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


En samling av [RevisionGroup](../revisiongroup/) objekt som representerar revisionsgrupper i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Returnerar antalet revisionsgrupper i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar en revisionsgrupp på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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


Du skapar inte instanser av den här klassen direkt. Använd egenskapen [Groups](../revisioncollection/get_groups/) för att hämta revisionsgrupper som finns i ett dokument.

## Exempel



Visar hur man skriver ut information om en grupp av revisioner i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```


Visar hur man hämtar en grupp av revisioner i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
