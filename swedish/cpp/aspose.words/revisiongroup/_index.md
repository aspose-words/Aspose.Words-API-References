---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionGroup class. Representerar en grupp av sekventiella Revision-objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 54000
url: /sv/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Representerar en grupp av sekventiella [Revision](../revision/) objekt. För att lära dig mer, besök dokumentationsartikeln [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Author](./get_author/)() | Hämtar författaren till denna revisionsgrupp. |
| [get_RevisionType](./get_revisiontype/)() | Hämtar typen av revisioner som ingår i denna grupp. |
| [get_Text](./get_text/)() | Returnerar infogad/borttagen/flyttad text eller beskrivning av formatändring. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
