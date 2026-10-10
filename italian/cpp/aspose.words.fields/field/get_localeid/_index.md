---
title: "Aspose::Words::Fields::Field::get_LocaleId method"
linktitle: "get_LocaleId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::get_LocaleId method. Ottiene o imposta il LCID del campo in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Ottiene o imposta il LCID del campo.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Esempi



Mostra come inserire un campo e lavorare con la sua impostazione locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un campo DATE, quindi stampa la data che visualizzerà.
// La cultura corrente del tuo thread determina la formattazione della data.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Modificare la cultura del nostro thread influenzerà il risultato del campo DATE.
// Un altro modo per far visualizzare al campo DATE una data in una cultura diversa è usare la sua proprietà LocaleId.
// In questo modo possiamo evitare di modificare la cultura del thread per ottenere questo effetto.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## Vedi anche

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
