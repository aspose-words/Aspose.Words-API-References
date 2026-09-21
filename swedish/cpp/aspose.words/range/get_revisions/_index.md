---
title: "Aspose::Words::Range::get_Revisions metod"
linktitle: "get_Revisions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::get_Revisions metod. Hämtar en samling av revisioner (spårade ändringar) som finns i detta intervall i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Hämtar en samling av revisioner (spårade ändringar) som finns i detta område.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Anmärkningar


Den returnerade samlingen är en "live"-samling, vilket betyder att om du tar bort delar av ett dokument som innehåller revisioner, så försvinner de raderade revisionerna automatiskt från denna samling.

## Exempel



Visar hur man arbetar med revisioner i ett intervall.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
for (auto&& revision : System::IterateOver(paragraph->get_Range()->get_Revisions()))
{
    if (revision->get_RevisionType() == Aspose::Words::RevisionType::Deletion)
    {
        revision->Accept();
    }
}

// Avvisa revisionerna i det första avsnittet.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## Se även

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
