---
title: "Aspose::Words::Fields::Field class"
linktitle: "Campo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field class. Rappresenta un campo di un documento Microsoft Word. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fields/field/
---
## Field class


Rappresenta un campo di documento Microsoft Word. Per saperne di più, visita l'articolo di documentazione.

```cpp
class Field : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](./get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](./get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](./get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](./get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](./get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](./get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](./get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](./get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](./get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](./get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](./get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](./getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](./getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Esegue lo scollegamento del campo. |
| [Update](./update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](./update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Note


Un campo in un documento Word è una struttura complessa composta da più nodi che includono l'inizio del campo, il codice del campo, il separatore del campo, il risultato del campo e la fine del campo. I [Fields](../) possono essere nidificati, contenere contenuti ricchi e coprire più paragrafi o sezioni in un documento. La classe [Field](./) è un oggetto "facade" che fornisce proprietà e metodi che consentono di lavorare con un campo come un unico oggetto.

Le proprietà [Start](./get_start/), [Separator](./get_separator/) e [End](./get_end/) puntano rispettivamente ai nodi di inizio, separatore e fine del campo.

Il contenuto tra l'inizio del campo e il separatore è il codice del campo. Il contenuto tra il separatore del campo e la fine del campo è il risultato del campo. Il codice del campo tipicamente consiste in uno o più oggetti [Run](../../aspose.words/run/) che specificano le istruzioni. L'applicazione di elaborazione dovrebbe eseguire il codice del campo per calcolare il risultato del campo.

Il processo di calcolo dei risultati dei campi è chiamato aggiornamento del campo. Aspose.Words può aggiornare i risultati dei campi della maggior parte dei tipi di campo esattamente nello stesso modo in cui lo fa Microsoft Word. In particolare, Aspose.Words può calcolare i risultati anche dei campi formula più complessi. Per calcolare il risultato di un singolo campo utilizza il metodo [Update](./update/). Per aggiornare i campi in tutto il documento utilizza [UpdateFields](../../aspose.words/document/updatefields/).

Puoi ottenere la versione in testo semplice del codice del campo utilizzando il metodo [GetFieldCode()](./getfieldcode/). Puoi ottenere e impostare la versione in testo semplice del risultato del campo utilizzando la proprietà [Result](./get_result/). Sia il codice del campo sia il risultato del campo possono contenere contenuti complessi, come campi nidificati, paragrafi, forme, tabelle e, in questo caso, potresti voler lavorare direttamente con i nodi del campo se hai bisogno di più controllo.

Non si creano istanze della classe [Field](./) direttamente. Per creare un nuovo campo utilizzare il metodo [InsertField()](../).

## Esempi



Mostra come inserire un campo in un documento utilizzando un codice di campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Questa variante del metodo InsertField aggiorna automaticamente i campi inseriti.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
