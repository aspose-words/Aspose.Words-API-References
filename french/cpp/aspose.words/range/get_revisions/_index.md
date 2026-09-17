---
title: "Méthode Aspose::Words::Range::get_Revisions"
linktitle: "get_Revisions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Range::get_Revisions. Obtient une collection de révisions (modifications suivies) qui existent dans cette plage en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Obtient une collection de révisions (modifications suivies) qui existent dans cette plage.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Remarques


La collection retournée est une collection "live", ce qui signifie que si vous supprimez des parties d'un document contenant des révisions, les révisions supprimées disparaîtront automatiquement de cette collection.

## Exemples



Montre comment travailler avec les révisions dans une plage.
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

// Rejette les révisions de la première section.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## Voir aussi

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
