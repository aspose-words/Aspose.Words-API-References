---
title: "Metodo Aspose::Words::RevisionCollection::RejectAll"
linktitle: "RejectAll"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::RevisionCollection::RejectAll. Rifiuta tutte le revisioni in questa collezione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/revisioncollection/rejectall/
---
## RevisionCollection::RejectAll method


Rifiuta tutte le revisioni in questa raccolta.

```cpp
void Aspose::Words::RevisionCollection::RejectAll()
```


## Esempi



Mostra come lavorare con la collezione di revisioni di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Questa collezione stessa contiene una collezione di gruppi di revisioni.
// Ogni gruppo è una sequenza di revisioni adiacenti.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Itera sulla collezione di gruppi e stampa il testo a cui la revisione si riferisce.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Ogni Run che una revisione colpisce ottiene un oggetto Revision corrispondente.
// La collezione delle revisioni è notevolmente più grande della forma condensata che abbiamo stampato sopra,
// a seconda di quanti Run abbiamo segmentato il documento durante la modifica con Microsoft Word.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // Uno StyleDefinitionChange influisce strettamente sugli stili e non sui nodi del documento. Questo significa che la "ParentStyle"
        // proprietà sarà sempre in uso, mentre la ParentNode sarà sempre null.
        // Poiché tutte le altre modifiche influenzano i nodi, la ParentNode sarà al contrario in uso, e la ParentStyle sarà null.
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

// Rifiuta tutte le revisioni tramite la collezione, ripristinando il documento alla sua forma originale.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## Vedi anche

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
