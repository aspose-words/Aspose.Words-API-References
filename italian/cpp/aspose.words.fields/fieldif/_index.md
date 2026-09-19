---
title: "Aspose::Words::Fields::FieldIf classe"
linktitle: "FieldIf"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIf classe. Implementa il campo IF. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 54000
url: /it/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


Implementa il campo IF. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Valuta la condizione. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Ottiene o imposta l'operatore di confronto. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](./get_end/)() override | Restituisce il nodo che rappresenta la fine del campo. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FalseText](./get_falsetext/)() | Ottiene o imposta il testo visualizzato se l'espressione di confronto è **false**. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LeftExpression](./get_leftexpression/)() | Ottiene o imposta la parte sinistra dell'espressione di confronto. |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_RightExpression](./get_rightexpression/)() | Ottiene o imposta la parte destra dell'espressione di confronto. |
| [get_Separator](./get_separator/)() override | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](./get_start/)() override | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_TrueText](./get_truetext/)() | Ottiene o imposta il testo visualizzato se l'espressione di confronto è true. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/). |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Note


Confronta i valori designati dalle espressioni [LeftExpression](./get_leftexpression/) e [RightExpression](./get_rightexpression/) utilizzando l'operatore designato da [ComparisonOperator](./get_comparisonoperator/).

Un campo nel seguente formato verrà utilizzato come origine per l'unione di stampa: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Esempi



Mostra come inserire un campo IF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// Il campo IF visualizzerà una stringa dalla proprietà "TrueText",
// oppure dalla proprietà "FalseText", a seconda della verità dell'affermazione che abbiamo costruito.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// In questo caso, "0 = 1" è errato, quindi il risultato visualizzato sarà "False".
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Questa volta l'affermazione è corretta, quindi il risultato visualizzato sarà "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
