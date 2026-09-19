---
title: "Metodo Aspose::Words::Range::get_Revisions"
linktitle: "get_Revisions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Range::get_Revisions. Ottiene una raccolta di revisioni (modifiche tracciate) presenti in questo intervallo in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Ottiene una collezione di revisioni (modifiche tracciate) presenti in questo intervallo.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Note


La raccolta restituita è una collezione "live", il che significa che se rimuovi parti di un documento che contengono revisioni, le revisioni eliminate scompariranno automaticamente da questa collezione.

## Esempi



Mostra come lavorare con le revisioni nell'intervallo.
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

// Rifiuta le revisioni della prima sezione.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## Vedi anche

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
