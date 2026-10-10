---
title: "Aspose::Words::Fields::FieldAutoNum classe"
linktitle: "FieldAutoNum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldAutoNum classe. Implementa il campo AUTONUM. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.fields/fieldautonum/
---
## FieldAutoNum class


Implementa il campo AUTONUM. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAutoNum : public Aspose::Words::Fields::Field,
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
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_SeparatorCharacter](./get_separatorcharacter/)() | Ottiene o imposta il carattere separatore da utilizzare. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SeparatorCharacter](./set_separatorcharacter/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter](./get_separatorcharacter/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come numerare i paragrafi usando campi autonum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ogni campo AUTONUM visualizza il valore corrente di un conteggio progressivo di campi AUTONUM,
// consentendoci di numerare automaticamente gli elementi come in un elenco numerato.
// Questo campo visualizzerà il numero "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Il carattere separatore, che appare nel risultato del campo immediatamente dopo il numero, è un punto per impostazione predefinita.
// Se lasciamo questa proprietà null, il nostro secondo campo AUTONUM visualizzerà "2." nel documento.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Possiamo impostare questa proprietà per utilizzare il primo carattere della sua stringa come nuovo carattere separatore.
// In questo caso, il nostro campo AUTONUM visualizzerà ora "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
