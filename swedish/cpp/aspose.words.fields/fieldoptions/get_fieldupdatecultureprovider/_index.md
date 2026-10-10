---
title: "Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider metod"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider metod. Hämtar eller anger en leverantör som returnerar ett kulturobjekt specifikt för varje enskilt fält i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Hämtar eller anger en leverantör som returnerar ett kulturobjekt specifikt för varje enskilt fält.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Anmärkningar


Leverantören begärs när värdet av [FieldUpdateCultureSource](../get_fieldupdateculturesource/) är [FieldCode](../../fieldupdateculturesource/).

Om leverantören är närvarande används kulturobjektet den returnerar för fältuppdateringen. Annars används en systemkultur.
## Se även

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
