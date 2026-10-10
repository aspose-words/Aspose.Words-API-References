---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat. Ottiene o imposta il valore che indica se il formato numerico è analizzato usando la cultura invariante o meno in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Ottiene o imposta il valore che indica se il formato numerico è analizzato usando la cultura invariata o meno.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Note


Quando questa proprietà è impostata su **true**, il formato numerico è preso da una cultura invariante.

Quando questa proprietà è impostata su **false**, il formato numerico è preso dalla cultura del thread corrente.

Il valore predefinito è **false**.

## Esempi



Mostra come formattare i numeri secondo la cultura invariante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// A volte, i campi potrebbero non formattare correttamente i numeri in alcune culture.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// Per risolvere questo, potremmo cambiare la cultura per l'intero thread.
// Un altro modo per risolvere questo è impostare questo flag,
// che fa sì che tutti i campi utilizzino la cultura invariante durante la formattazione dei numeri.
// In questo modo ci consente di evitare di cambiare la cultura per l'intero thread.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## Vedi anche

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
