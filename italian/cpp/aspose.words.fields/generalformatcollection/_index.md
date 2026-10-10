---
title: "Classe Aspose::Words::Fields::GeneralFormatCollection"
linktitle: "GeneralFormatCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::GeneralFormatCollection. Rappresenta una collezione tipizzata di formati generali. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 114000
url: /it/cpp/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class


Rappresenta una raccolta tipizzata di formati generali. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class GeneralFormatCollection : public System::Collections::Generic::IEnumerable<Aspose::Words::Fields::GeneralFormat>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(Aspose::Words::Fields::GeneralFormat) | Aggiunge un formato generale alla collezione. |
| [get_Count](./get_count/)() | Restituisce il numero totale di elementi nella collezione. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce un formato generale all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(Aspose::Words::Fields::GeneralFormat) | Rimuove tutte le occorrenze del formato generale specificato dalla collezione. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un'occorrenza di formato generale all'indice specificato. |
| static [Type](./type/)() |  |

## Esempi



Mostra come formattare i risultati dei campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Usa un document builder per inserire un campo che visualizza un risultato senza alcun formato applicato.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Possiamo applicare un formato al risultato di un campo usando le proprietà del campo.
// Di seguito sono riportati tre tipi di formati che possiamo applicare al risultato di un campo.
// 1 -  Formato numerico:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Formato data/ora:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Formato generale:
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// Possiamo rimuovere i nostri formati per ripristinare il risultato del campo nella sua forma originale.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
