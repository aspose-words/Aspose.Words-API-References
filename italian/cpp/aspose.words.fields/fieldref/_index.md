---
title: "Aspose::Words::Fields::FieldRef class"
linktitle: "FieldRef"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldRef class. Implementa il campo REF. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 85000
url: /it/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Implementa il campo REF. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Ottiene o imposta il nome del segnalibro di riferimento. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](./get_end/)() override | Restituisce il nodo che rappresenta la fine del campo. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Ottiene se incrementare i numeri di nota a piè di pagina, nota finale e annotazione contrassegnati dal segnalibro, e inserire il testo corrispondente della nota a piè di pagina, nota finale e commento. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Ottiene se creare un collegamento ipertestuale al paragrafo contrassegnato. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Ottiene se inserire il numero del paragrafo di riferimento esattamente come appare nel documento. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Ottiene se inserire il numero del paragrafo di riferimento nel contesto completo. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Ottiene se inserire il numero del paragrafo di riferimento nel contesto relativo. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Ottiene se inserire la posizione relativa del paragrafo di riferimento. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_NumberSeparator](./get_numberseparator/)() | Ottiene la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](./get_separator/)() override | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](./get_start/)() override | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Ottiene se sopprimere i caratteri non delimitatori. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Imposta se incrementare i numeri di nota a piè di pagina, nota finale e annotazione contrassegnati dal segnalibro, e inserire il testo corrispondente della nota a piè di pagina, nota finale e commento. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Imposta se creare un collegamento ipertestuale al paragrafo contrassegnato. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Imposta se inserire il numero del paragrafo di riferimento esattamente come appare nel documento. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Imposta se inserire il numero del paragrafo di riferimento nel contesto completo. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Imposta se inserire il numero del paragrafo del paragrafo di riferimento nel contesto relativo. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Imposta se inserire la posizione relativa del paragrafo di riferimento. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Imposta se sopprimere i caratteri non delimitatori. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come creare testo contrassegnato con un campo SET e poi visualizzarlo nel documento usando un campo REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nomina il testo contrassegnato con un campo SET.
// Questo campo si riferisce al "bookmark" non a una struttura di segnalibro che appare nel testo, ma a una variabile nominata.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Fai riferimento al segnalibro per nome in un campo REF e visualizza il suo contenuto.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
