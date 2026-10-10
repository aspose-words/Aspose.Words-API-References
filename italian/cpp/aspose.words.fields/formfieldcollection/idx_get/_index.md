---
title: "Metodo idx_get di Aspose::Words::Fields::FormFieldCollection"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo idx_get di Aspose::Words::Fields::FormFieldCollection. Restituisce un campo modulo per nome segnalibro in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fields/formfieldcollection/idx_get/
---
## FormFieldCollection::idx_get(const System::String\&) method


Restituisce un campo modulo per nome segnalibro.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(const System::String &bookmarkName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nome segnalibro non sensibile a maiuscole/minuscole. |

## Vedi anche

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FormFieldCollection::idx_get(int32_t) method


Restituisce un campo modulo all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella collezione. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Vedi anche

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
