---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionGroup class. Stellt eine Gruppe von aufeinanderfolgenden Revision-Objekten dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 54000
url: /de/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Stellt eine Gruppe von aufeinanderfolgenden [Revision](../revision/)-Objekten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Author](./get_author/)() | Liefert den Autor dieser Revisionsgruppe. |
| [get_RevisionType](./get_revisiontype/)() | Liefert den Typ der in dieser Gruppe enthaltenen Revisionen. |
| [get_Text](./get_text/)() | Gibt eingefügten/gelöschten/verschobenen Text oder eine Beschreibung der Formatänderung zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
