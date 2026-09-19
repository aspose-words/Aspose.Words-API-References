---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField metodo"
linktitle: "MoveToMergeField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField metodo. Sposta il cursore in una posizione subito oltre il campo di unione specificato e rimuove il campo di unione in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | const System::String\& | Il nome del campo di unione mail, senza distinzione tra maiuscole e minuscole. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Note


Nota che questo metodo elimina il campo di unione dal documento dopo aver spostato il cursore.

## Esempi



Mostra come riempire i MERGEFIELD con i dati usando un document builder invece di un'unione di stampa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci alcuni MERGEFIELD, che accettano dati dalle colonne con lo stesso nome in una fonte dati durante un'unione di stampa,
// e poi riempili manualmente.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Sposta il campo di unione sul campo di unione specificato.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | const System::String\& | Il nome del campo di unione mail, senza distinzione tra maiuscole e minuscole. |
| isAfter | bool | Quando **true**, sposta il cursore in modo che sia dopo la fine del campo. Quando **false**, sposta il cursore in modo che sia prima dell'inizio del campo. |
| isDeleteField | bool | Quando **true**, elimina il campo di unione. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

## Esempi



Mostra come inserire i campi e spostare il cursore del document builder su di essi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Sposta il cursore sul primo MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Nota che il cursore è posizionato immediatamente dopo il primo MERGEFIELD e prima del secondo.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Se desideriamo modificare il codice campo o il contenuto del campo usando il builder,
// il suo cursore dovrebbe trovarsi all'interno di un campo.
// Per posizionarlo all'interno di un campo, dovremmo chiamare il metodo MoveTo del document builder
// e passare il nodo di inizio o di separatore del campo come argomento.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
