---
title: "Metodo Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture"
linktitle: "GetCulture"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture. Restituisce un oggetto CultureInfo da utilizzare durante l'aggiornamento del campo in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


Restituisce un oggetto **CultureInfo** da utilizzare durante l'aggiornamento del campo.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| cultura | System::String | Il nome della cultura richiesta per il campo in fase di aggiornamento. |
| campo | System::SharedPtr\<Aspose::Words::Fields::Field\> | Il campo in fase di aggiornamento. |

### ReturnValue

L'oggetto cultura che dovrebbe essere utilizzato per l'aggiornamento del campo.

## Vedi anche

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
