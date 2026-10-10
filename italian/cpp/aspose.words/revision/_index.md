---
title: "Classe Aspose::Words::Revision"
linktitle: "Revisione"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Revision. Rappresenta una revisione (modifica tracciata) in un nodo o stile di documento. Usa RevisionType per verificare il tipo di questa revisione. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 52000
url: /it/cpp/aspose.words/revision/
---
## Revision class


Rappresenta una revisione (modifica tracciata) in un nodo o stile di documento. Usa [RevisionType](./get_revisiontype/) per verificare il tipo di questa revisione. Per saperne di più, visita l'articolo di documentazione [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class Revision : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)() | Accetta questa revisione. |
| [get_Author](./get_author/)() | Ottiene o imposta l'autore di questa revisione. Non può essere una stringa vuota o **null**. |
| [get_DateTime](./get_datetime/)() | Ottiene o imposta la data/ora di questa revisione. |
| [get_Group](./get_group/)() | Ottiene il gruppo di revisione. Restituisce **null** se la revisione non appartiene a nessun gruppo. |
| [get_ParentNode](./get_parentnode/)() | Ottiene il nodo genitore immediato (proprietario) di questa revisione. Questa proprietà funzionerà per qualsiasi tipo di revisione diverso da [StyleDefinitionChange](../revisiontype/). |
| [get_ParentStyle](./get_parentstyle/)() | Ottiene lo stile genitore immediato (proprietario) di questa revisione. Questa proprietà funzionerà solo per il tipo di revisione [StyleDefinitionChange](../revisiontype/). |
| [get_RevisionType](./get_revisiontype/)() const | Ottiene il tipo di questa revisione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Reject](./reject/)() | Rifiuta questa revisione. |
| [set_Author](./set_author/)(const System::String\&) | Setter per [Aspose::Words::Revision::get_Author](./get_author/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Setter per [Aspose::Words::Revision::get_DateTime](./get_datetime/). |
| static [Type](./type/)() |  |

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
