---
title: "Aspose::Words::RevisionType enum"
linktitle: "RevisionType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionType enum. Specifica il tipo di modifica tracciata nella Revision in C++."
type: docs
weight: 113000
url: /it/cpp/aspose.words/revisiontype/
---
## RevisionType enum


Specifica il tipo di modifica tracciata in [Revision](../revision/).

```cpp
enum class RevisionType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Insertion | 0 | Nuovo contenuto è stato inserito nel documento. |
| Deletion | 1 | Il contenuto è stato rimosso dal documento. |
| FormatChange | 2 | È stata applicata una modifica di formattazione al nodo genitore. |
| StyleDefinitionChange | 3 | È stata applicata una modifica di formattazione allo stile genitore. |
| Spostamento | 4 | Il contenuto è stato spostato nel documento. |


## Esempi



Mostra come lavorare con le revisioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// La modifica normale del documento non conta come revisione.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// Per registrare le nostre modifiche come revisioni, è necessario dichiarare un autore e poi iniziare a tracciarle.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Questa opzione corrisponde a "Review" -> "Tracking" -> "Track Changes" in Microsoft Word.
// Il metodo "StartTrackRevisions" non influisce sul suo valore,
// e il documento sta tracciando le revisioni programmaticamente nonostante abbia il valore "false".
// Se apriamo questo documento con Microsoft Word, non tracerà le revisioni.
ASSERT_FALSE(doc->get_TrackRevisions());

// Abbiamo aggiunto testo usando il document builder, quindi la prima revisione è una revisione di tipo inserimento.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Rimuovi un run per creare una revisione di tipo cancellazione.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Aggiungere una nuova revisione la posiziona all'inizio della raccolta di revisioni.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Le revisioni di inserimento appaiono nel corpo del documento anche prima di accettare/rifiutare la revisione.
// Rifiutare la revisione rimuoverà i suoi nodi dal corpo. Al contrario, i nodi che compongono le revisioni di cancellazione
// rimangono comunque nel documento finché non accettiamo la revisione.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Accettare la revisione di cancellazione rimuoverà il nodo genitore dal testo del paragrafo
// e poi rimuoverà la revisione stessa dalla raccolta.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Ora sposta il nodo per creare un tipo di revisione di spostamento.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// La revisione di spostamento è ora all'indice 1. Rifiuta la revisione per scartare il suo contenuto.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
