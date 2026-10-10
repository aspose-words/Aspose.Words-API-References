---
title: "Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider-Methode"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider method. Ruft einen Anbieter ab oder legt ihn fest, der ein kulturspezifisches Objekt für jedes einzelne Feld in C++ zurückgibt."
type: docs
weight: 10000
url: /de/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Liest oder setzt einen Anbieter, der ein kulturspezifisches Objekt für jedes einzelne Feld zurückgibt.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Hinweise


Der Anbieter wird angefordert, wenn der Wert von [FieldUpdateCultureSource](../get_fieldupdateculturesource/) [FieldCode](../../fieldupdateculturesource/) ist.

Ist der Anbieter vorhanden, wird das von ihm zurückgegebene Kulturobjekt für die Feldaktualisierung verwendet. Andernfalls wird eine Systemkultur verwendet.
## Siehe auch

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
