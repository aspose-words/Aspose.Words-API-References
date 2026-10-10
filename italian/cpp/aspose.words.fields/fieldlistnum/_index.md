---
title: "Aspose::Words::Fields::FieldListNum class"
linktitle: "FieldListNum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldListNum class. Implementa il campo LISTNUM. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 64000
url: /it/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


Implementa il campo LISTNUM. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_HasListName](./get_haslistname/)() | Restituisce un valore che indica se il nome di una definizione di numerazione astratta è fornito dal codice del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_ListLevel](./get_listlevel/)() | Ottiene o imposta il livello nell'elenco, sovrascrivendo il comportamento predefinito del campo. |
| [get_ListName](./get_listname/)() | Ottiene o imposta il nome della definizione di numerazione astratta utilizzata per la numerazione. |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_StartingNumber](./get_startingnumber/)() | Ottiene o imposta il valore iniziale per questo campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come numerare i paragrafi con i campi LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// I campi LISTNUM mostrano un numero che si incrementa ad ogni campo LISTNUM.
// Questi campi hanno anche una varietà di opzioni che ci permettono di usarli per emulare elenchi numerati.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Gli elenchi iniziano a contare da 1 per impostazione predefinita, ma possiamo impostare questo numero a un valore diverso, ad esempio 0.
// Questo campo mostrerà "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// I campi LISTNUM mantengono conteggi separati per ogni livello di elenco.
// Inserire un campo LISTNUM nello stesso paragrafo di un altro campo LISTNUM
// aumenta il livello dell'elenco invece del conteggio.
// Il campo successivo continuerà il conteggio che abbiamo iniziato sopra e mostrerà un valore di "1" al livello di elenco 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Questo campo inizierà un conteggio al livello di elenco 2. Mostrerà un valore di "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Questo campo inizierà un conteggio al livello di elenco 3. Mostrerà un valore di "1".
// Livelli di elenco diversi hanno formattazioni diverse,
// quindi questi campi combinati mostreranno un valore di "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Il prossimo campo LISTNUM che inseriamo continuerà il conteggio al livello di elenco
// su cui era il campo LISTNUM precedente.
// Possiamo usare la proprietà "ListLevel" per passare a un livello di elenco diverso.
// Se questo campo LISTNUM rimanesse al livello di elenco 3, mostrerebbe "ii)",
// ma, poiché lo abbiamo spostato al livello di elenco 2, continua il conteggio a quel livello e mostra "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Possiamo impostare la proprietà ListName per far sì che il campo emuli un tipo di campo AUTONUM diverso.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// e "LegalDefault" emula i campi AUTONUMLGL.
// Il nome dell'elenco "OutlineDefault" con 1 come numero iniziale produrrà la visualizzazione di "I.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// Il ListName non viene trasferito dal campo precedente, quindi dovremo impostarlo per ogni nuovo campo.
// Questo campo continua il conteggio con un nome elenco diverso e visualizza "II.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
