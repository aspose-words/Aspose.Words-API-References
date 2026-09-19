---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider. Ottiene o imposta un provider che restituisce un oggetto cultura specifico per ciascun campo particolare in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Ottiene o imposta un provider che restituisce un oggetto cultura specifico per ciascun campo particolare.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Note


Il provider viene richiesto quando il valore di [FieldUpdateCultureSource](../get_fieldupdateculturesource/) è [FieldCode](../../fieldupdateculturesource/).

Se il provider è presente, l'oggetto cultura restituito viene utilizzato per l'aggiornamento del campo. Altrimenti, viene utilizzata una cultura di sistema.
## Vedi anche

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
