---
title: "Aspose::Words::RevisionGroupCollection class"
linktitle: "RevisionGroupCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionGroupCollection class. Eine Sammlung von RevisionGroup‑Objekten, die Revisionsgruppen im Dokument darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 55000
url: /de/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


Eine Sammlung von [RevisionGroup](../revisiongroup/)-Objekten, die Revisionsgruppen im Dokument darstellen. Weitere Informationen finden Sie im Dokumentationsartikel [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der Revisionsgruppen in der Sammlung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt eine Revisionsgruppe am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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


Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die Eigenschaft [Groups](../revisioncollection/get_groups/), um die im Dokument vorhandenen Revisionsgruppen abzurufen.

## Beispiele



Zeigt, wie man Informationen über eine Gruppe von Revisionen in einem Dokument ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```


Zeigt, wie man eine Gruppe von Revisionen in einem Dokument erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
