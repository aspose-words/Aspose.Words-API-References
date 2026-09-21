---
title: "Aspose::Words::Revision::get_ParentStyle metod"
linktitle: "get_ParentStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Revision::get_ParentStyle metod. Hämtar den omedelbara förälderstilen (ägaren) för den här revisionen. Denna egenskap fungerar endast för revisionstypen StyleDefinitionChange i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/revision/get_parentstyle/
---
## Revision::get_ParentStyle method


Hämtar den omedelbara förälderstilen (ägaren) för den här revisionen. Denna egenskap fungerar endast för [StyleDefinitionChange](../../revisiontype/) revisionstypen.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Revision::get_ParentStyle()
```


## Exempel



Visar hur man arbetar med ett dokuments samling av revisioner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Denna samling har i sig själv en samling av revisionsgrupper.
// Varje grupp är en sekvens av intilliggande revisioner.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Iterera över samlingen av grupper och skriv ut den text som revisionen gäller.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Varje Run som en revision påverkar får ett motsvarande Revision-objekt.
// Revisionernas samling är avsevärt större än den kondenserade formen vi skrev ut ovan,
// beroende på hur många Run vi har segmenterat dokumentet i under Microsoft Word-redigering.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // En StyleDefinitionChange påverkar strikt stilar och inte dokumentnoder. Detta betyder att "ParentStyle"
        // egenskapen kommer alltid att vara i bruk, medan ParentNode alltid kommer att vara null.
        // Eftersom alla andra ändringar påverkar noder, kommer ParentNode omvänt att vara i bruk, och ParentStyle kommer att vara null.
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

// Avvisa alla revisioner via samlingen, vilket återställer dokumentet till dess ursprungliga form.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## Se även

* Class [Style](../../style/)
* Class [Revision](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
