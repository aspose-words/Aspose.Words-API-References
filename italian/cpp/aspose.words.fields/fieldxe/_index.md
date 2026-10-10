---
title: "classe Aspose::Words::Fields::FieldXE"
linktitle: "FieldXE"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Fields::FieldXE. Implementa il campo XE. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 111000
url: /it/cpp/aspose.words.fields/fieldxe/
---
## FieldXE class


Implementa il campo XE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldXE : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_EntryType](./get_entrytype/)() | Ottiene o imposta un tipo di voce di indice. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsBold](./get_isbold/)() | Ottiene o imposta se applicare la formattazione grassetto al numero di pagina della voce. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsItalic](./get_isitalic/)() | Ottiene o imposta se applicare la formattazione corsivo al numero di pagina della voce. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_PageNumberReplacement](./get_pagenumberreplacement/)() | Ottiene o imposta il testo usato al posto di un numero di pagina. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Ottiene o imposta il nome del segnalibro che segna un intervallo di pagine inserito come numero di pagina della voce. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Text](./get_text/)() | Ottiene o imposta il testo della voce. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_Yomi](./get_yomi/)() | Ottiene o imposta lo yomi (primo carattere fonetico per l'ordinamento degli indici) della voce di indice. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldXE::get_EntryType](./get_entrytype/). |
| [set_IsBold](./set_isbold/)(bool) | Impostatore per [Aspose::Words::Fields::FieldXE::get_IsBold](./get_isbold/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsItalic](./set_isitalic/)(bool) | Impostatore per [Aspose::Words::Fields::FieldXE::get_IsItalic](./get_isitalic/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberReplacement](./set_pagenumberreplacement/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldXE::get_PageNumberReplacement](./get_pagenumberreplacement/). |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName](./get_pagerangebookmarkname/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldXE::get_Text](./get_text/). |
| [set_Yomi](./set_yomi/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldXE::get_Yomi](./get_yomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come creare un campo INDEX e poi utilizzare i campi XE per popolarlo con voci.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro
// e la pagina contenente il campo XE sul lato destro.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
// il campo INDEX li raggrupperà in un'unica voce.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Configura il campo INDEX in modo che visualizzi solo i campi XE che si trovano entro i limiti
// di un segnalibro chiamato "MainBookmark" e le cui proprietà "EntryType" hanno valore "A".
// Per entrambi i campi INDEX e XE, la proprietà "EntryType" utilizza solo il primo carattere del suo valore stringa.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// In una nuova pagina, avvia il segnalibro con un nome che corrisponde al valore
// della proprietà "BookmarkName" del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// Il campo INDEX prenderà questa voce perché si trova all'interno del segnalibro,
// e il suo tipo di voce corrisponde anche al tipo di voce del campo INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Inserisci un campo XE che non apparirà nell'INDEX perché i tipi di voce non corrispondono.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Chiudi il segnalibro e inserisci un campo XE successivamente.
// È dello stesso tipo del campo INDEX, ma non apparirà
// poiché è al di fuori dei confini del segnalibro.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```


Mostra come popolare un campo INDEX con voci usando i campi XE e anche modificare il suo aspetto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
// il campo INDEX li raggrupperà in un'unica voce.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Impostare il valore di questa proprietà su "A" raggrupperà tutte le voci per la loro prima lettera,
// e posizionerà quella lettera in maiuscolo sopra ogni gruppo.
index->set_Heading(u"A");

// Imposta la tabella creata dal campo INDEX per estendersi su 2 colonne.
index->set_NumberOfColumns(u"2");

// Imposta che tutte le voci con lettere iniziali al di fuori dell'intervallo di caratteri "a-c" vengano omesse.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// I prossimi due campi XE appariranno sotto l'intestazione "A",
// con i rispettivi stili di testo applicati anche ai numeri di pagina.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Entrambi i prossimi due campi XE saranno sotto le intestazioni "B" e "C" nel sommario dei campi INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// I campi INDEX ordinano tutte le voci alfabeticamente, quindi questa voce apparirà sotto "A" insieme alle altre due.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Questa voce non apparirà perché inizia con la lettera "D",
// che è al di fuori dell'intervallo di caratteri "a-c" definito dalla proprietà LetterRange del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
