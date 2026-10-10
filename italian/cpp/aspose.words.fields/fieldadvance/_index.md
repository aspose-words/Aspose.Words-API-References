---
title: "Classe Aspose::Words::Fields::FieldAdvance"
linktitle: "FieldAdvance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::FieldAdvance. Implementa il campo ADVANCE. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.fields/fieldadvance/
---
## FieldAdvance class


Implementa il campo ADVANCE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAdvance : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_DownOffset](./get_downoffset/)() | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verso il basso. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato orizzontalmente dal bordo sinistro della colonna, del riquadro o della casella di testo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LeftOffset](./get_leftoffset/)() | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a sinistra. |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_RightOffset](./get_rightoffset/)() | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a destra. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_UpOffset](./get_upoffset/)() | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verso l'alto. |
| [get_VerticalPosition](./get_verticalposition/)() | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verticalmente dal bordo superiore della pagina. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_DownOffset](./set_downoffset/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldAdvance::get_DownOffset](./get_downoffset/). |
| [set_HorizontalPosition](./set_horizontalposition/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition](./get_horizontalposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftOffset](./set_leftoffset/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldAdvance::get_LeftOffset](./get_leftoffset/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightOffset](./set_rightoffset/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldAdvance::get_RightOffset](./get_rightoffset/). |
| [set_UpOffset](./set_upoffset/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldAdvance::get_UpOffset](./get_upoffset/). |
| [set_VerticalPosition](./set_verticalposition/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldAdvance::get_VerticalPosition](./get_verticalposition/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come inserire un campo ADVANCE e modificare le sue proprietà.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Di seguito sono riportati due modi per utilizzare il campo ADVANCE per regolare la posizione del testo che lo segue.
// Gli effetti di un campo ADVANCE continuano ad essere applicati fino alla fine del paragrafo,
// o un altro campo ADVANCE aggiorna i valori di offset/coordinate.
// 1 -  Specificare un offset direzionale:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Spostare il testo in una posizione specificata dalle coordinate:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
