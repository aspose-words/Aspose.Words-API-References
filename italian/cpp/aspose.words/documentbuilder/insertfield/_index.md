---
title: "Aspose::Words::DocumentBuilder::InsertField metodo"
linktitle: "InsertField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertField metodo. Inserisce un campo Word in un documento e opzionalmente aggiorna il risultato del campo in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Inserisce un campo Word in un documento e opzionalmente aggiorna il risultato del campo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Il tipo del campo da aggiungere. |
| updateField | bool | Specifica se aggiornare il campo immediatamente. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.
## Note


Questo metodo inserisce un campo in un documento. Aspose.Words può aggiornare campi della maggior parte dei tipi, ma non tutti. Per ulteriori dettagli vedi il sovraccarico [InsertField()](../).

## Esempi



Mostra come inserire un campo in un documento usando FieldType.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci due campi passando un flag che determina se aggiornarli mentre il builder li inserisce.
// In alcuni casi, l'aggiornamento dei campi può essere computazionalmente costoso, e potrebbe essere una buona idea posticipare l'aggiornamento.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // Dovremo aggiornare questi campi manualmente usando i metodi di aggiornamento.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Inserisce un campo Word in un documento e aggiorna il risultato del campo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | const System::String\& | Il codice campo da inserire (senza parentesi graffe). |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.
## Note


Questo metodo inserisce un campo in un documento e aggiorna immediatamente il risultato del campo. Aspose.Words può aggiornare i campi della maggior parte dei tipi, ma non tutti. Per ulteriori dettagli vedere la sovraccarico [InsertField()](../).

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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Inserisce un campo Word in un documento senza aggiornare il risultato del campo.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldCode | const System::String\& | Il codice campo da inserire (senza parentesi graffe). |
| fieldValue | const System::String\& | Il valore del campo da inserire. Passare **null** per i campi che non hanno un valore. |

### ReturnValue

Un oggetto [Field](../../../aspose.words.fields/field/) che rappresenta il campo inserito.
## Note


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

È possibile alternare tra la visualizzazione dei codici campo e dei risultati nel documento in Microsoft Word usando la scorciatoia da tastiera Alt+F9. I codici campo appaiono tra parentesi graffe ( { } ).

Per creare un campo, è necessario specificare un tipo di campo, un codice campo e un valore campo "segnaposto". Se non sei sicuro della sintassi di un particolare codice campo, crea prima il campo in Microsoft Word e poi passa alla visualizzazione del suo codice campo.

Aspose.Words può calcolare i risultati dei campi per la maggior parte dei tipi di campo, ma questo metodo non aggiorna automaticamente il risultato del campo. Poiché il risultato del campo non viene calcolato automaticamente, ci si aspetta di passare una stringa (o anche una stringa vuota) che verrà inserita nel risultato del campo. Questo valore rimarrà nel risultato del campo come segnaposto finché il campo non verrà aggiornato. Per aggiornare il risultato del campo è possibile chiamare [Update](../../../aspose.words.fields/field/update/) sull'oggetto campo restituito o [UpdateFields](../../document/updatefields/) per aggiornare i campi in tutto il documento.

## Esempi



Mostra come impostare la numerazione delle pagine in una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Sposta il document builder nell'intestazione primaria della prima sezione,
// che verrà visualizzata su ogni pagina di quella sezione.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Inserisci un campo PAGE, che visualizzerà il numero della pagina corrente.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configura la sezione in modo che il conteggio delle pagine visualizzato dai campi PAGE inizi da 5.
// Inoltre, configura tutti i campi PAGE per visualizzare i loro numeri di pagina usando numeri romani maiuscoli.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Crea un'altra intestazione primaria per la seconda sezione, con un altro campo PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configura la sezione in modo che il conteggio delle pagine visualizzato dai campi PAGE inizi da 10.
// Inoltre, configura tutti i campi PAGE per visualizzare i loro numeri di pagina usando numeri arabi.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Vedi anche

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
