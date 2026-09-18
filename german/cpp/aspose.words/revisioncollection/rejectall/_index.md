---
title: "Aspose::Words::RevisionCollection::RejectAll Methode"
linktitle: "RejectAll"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionCollection::RejectAll Methode. Verwirft alle Revisionen in dieser Sammlung in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/revisioncollection/rejectall/
---
## RevisionCollection::RejectAll method


Verwirft alle Revisionen in dieser Sammlung.

```cpp
void Aspose::Words::RevisionCollection::RejectAll()
```


## Beispiele



Zeigt, wie man mit der Revisionssammlung eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Diese Sammlung enthält selbst eine Sammlung von Revisionsgruppen.
// Jede Gruppe ist eine Sequenz benachbarter Revisionen.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Iterieren Sie über die Sammlung von Gruppen und geben Sie den Text aus, den die Revision betrifft.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Jeder Run, den eine Revision beeinflusst, erhält ein entsprechendes Revision-Objekt.
// Die Revisionssammlung ist deutlich größer als die komprimierte Form, die wir oben ausgegeben haben,
// abhängig davon, in wie viele Runs wir das Dokument während der Bearbeitung in Microsoft Word segmentiert haben.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // Ein StyleDefinitionChange wirkt sich ausschließlich auf Stile und nicht auf Dokumentknoten aus. Das bedeutet, dass die "ParentStyle"
        // Eigenschaft immer verwendet wird, während ParentNode stets null ist.
        // Da alle anderen Änderungen Knoten betreffen, wird ParentNode im Gegenzug verwendet werden, und ParentStyle wird null sein.
        if (e->get_Current()->get_RevisionType() == Aspose::Words::RevisionType::StyleDefinitionChange)
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name())) << std::endl;
        }
        else
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentNode()->GetText().Trim())) << std::endl;
        }
    }
}

// Verwerfen Sie alle Revisionen über die Sammlung und stellen Sie das Dokument in seine ursprüngliche Form zurück.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## Siehe auch

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
