---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat"
linktitle: "get_LegacyNumberFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat. Ottiene o imposta il valore che indica se il formato numerico legacy (precedente ad AW 13.10) per i campi è abilitato o meno in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Ottiene o imposta il valore che indica se il formato numerico legacy (precedente a AW 13.10) per i campi è abilitato o meno.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Note


Quando questa proprietà è impostata su **true**, il simbolo modello "#" funziona come in .net: sostituisce il segno di cancelletto con la cifra corrispondente se presente; altrimenti, nessun simbolo appare nella stringa risultante.

Quando questa proprietà è impostata su **false**, il simbolo modello "#" funziona come MS Word: questo elemento di formato specifica le posizioni numeriche necessarie da visualizzare nel risultato. Se il risultato non include una cifra in quella posizione, MS Word visualizza uno spazio. Per esempio, { = 9 + 6 \\# $### } visualizza $ 15.

Il valore predefinito è **false**.

## Esempi



Mostra come abilitare la formattazione numerica legacy per i campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## Vedi anche

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
