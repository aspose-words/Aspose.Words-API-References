---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream metod"
linktitle: "get_CssStream"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream metod. Tillåter att ange strömmen där CSS‑informationen ska sparas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Tillåter att ange strömmen där CSS‑informationen ska sparas.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Anmärkningar


Denna egenskap tillåter dig att spara CSS‑information till en ström.

Standardvärdet är **null**. Denna egenskap förhindrar inte att CSS‑information sparas till en fil eller bäddas in i HTML‑dokumentet. För att förhindra export av CSS, använd egenskapen [IsExportNeeded](../get_isexportneeded/).

Med [ICssSavingCallback](../../icsssavingcallback/) kan du inte ersätta CSS med en annan. Den är avsedd endast för att spara CSS till en ström.

## Se även

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
