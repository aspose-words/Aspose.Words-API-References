---
title: "Aspose::Words::Fields::FieldDate class"
linktitle: "FieldDate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldDate class. Implementa il campo DATE. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words.fields/fielddate/
---
## FieldDate class


Implementa il campo DATE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDate : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                  public Aspose::Words::Fields::IFieldWithCalendar
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
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_UseLastFormat](./get_uselastformat/)() | Ottiene o imposta se utilizzare un formato usato per ultimo dall'applicazione host durante l'inserimento di un nuovo campo DATE. |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() override | Ottiene o imposta se utilizzare il calendario lunare Hijri o il calendario lunare ebraico. |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() override | Ottiene o imposta se utilizzare il calendario dell'Era Saka. |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() override | Ottiene o imposta se utilizzare il calendario Um-al-Qura. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_UseLastFormat](./set_uselastformat/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDate::get_UseLastFormat](./get_uselastformat/). |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDate::get_UseLunarCalendar](./get_uselunarcalendar/). |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDate::get_UseSakaEraCalendar](./usesakaeracalendar/). |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar](./useumalquracalendar/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come utilizzare i campi DATE per visualizzare le date secondo diversi tipi di calendari.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se vogliamo che il testo nel documento mostri sempre la data corretta, possiamo usare un campo DATE.
// Di seguito sono riportati tre tipi di calendari culturali che un campo DATE può utilizzare per visualizzare una data.
// 1 -  Calendario lunare islamico:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Calendario Umm al-Qura:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Calendario nazionale indiano:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Inserisci un campo DATE e imposta il suo tipo di calendario a quello usato per ultimo dall'applicazione host.
// In Microsoft Word, il tipo sarà quello più recentemente usato nella finestra di dialogo Inserisci -> Testo -> Data e ora.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
