---
title: "Aspose::Words::Range::get_Revisions Methode"
linktitle: "get_Revisions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range::get_Revisions Methode. Gibt eine Sammlung von Revisionen (nachverfolgte Änderungen) zurück, die in diesem Bereich existieren, in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Ruft eine Sammlung von Revisionen (nachverfolgte Änderungen) ab, die in diesem Bereich existieren.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Hinweise


Die zurückgegebene Sammlung ist eine "Live"-Sammlung, was bedeutet, dass wenn Sie Teile eines Dokuments entfernen, die Revisionen enthalten, die gelöschten Revisionen automatisch aus dieser Sammlung verschwinden.

## Beispiele



Zeigt, wie man mit Revisionen im Bereich arbeitet.
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

// Verwerfe die Revisionen des ersten Abschnitts.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## Siehe auch

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
