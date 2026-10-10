---
title: "Aspose::Words::Fields::Field::Unlink metodo"
linktitle: "Scollega"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::Unlink metodo. Esegue lo scollegamento del campo in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Esegue lo scollegamento del campo.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Note


Sostituisce il campo con il suo risultato più recente.

Alcuni campi, come i campi XE (Voce di indice) e i campi SEQ (Sequenza), non possono essere scollegati.

## Esempi



Mostra come scollegare un campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## Vedi anche

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
