---
title: "Metodo Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields"
linktitle: "get_UpdateDirtyFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields. Specifica se aggiornare i campi con l'attributo dirty in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.loading/loadoptions/get_updatedirtyfields/
---
## LoadOptions::get_UpdateDirtyFields method


Specifica se aggiornare i campi con l'attributo **dirty**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields() const
```


## Esempi



Mostra come utilizzare la proprietà speciale per aggiornare il risultato del campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fornisci il valore della proprietà incorporata \"Author\" del documento, quindi visualizzalo con un campo.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Aggiorna la proprietà. Il campo mostra ancora il valore precedente.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Poiché il valore del campo è obsoleto, possiamo contrassegnarlo come \"dirty\".
// Questo valore rimarrà obsoleto finché non aggiorniamo manualmente il campo con il metodo Field.Update().
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Se salviamo senza chiamare un metodo di aggiornamento,
    // il campo continuerà a mostrare il valore obsoleto nel documento di output.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // L'oggetto LoadOptions ha un'opzione per aggiornare tutti i campi
    // contrassegnati come \"dirty\" durante il caricamento del documento.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Aggiornare i campi dirty in questo modo imposta automaticamente il loro flag \"IsDirty\" su false.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
