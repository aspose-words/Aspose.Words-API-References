---
title: "Metodo Aspose::Words::Fields::FieldListNum::get_StartingNumber"
linktitle: "get_StartingNumber"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldListNum::get_StartingNumber. Ottiene o imposta il valore iniziale per questo campo in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fields/fieldlistnum/get_startingnumber/
---
## FieldListNum::get_StartingNumber method


Ottiene o imposta il valore iniziale per questo campo.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_StartingNumber()
```


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

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
