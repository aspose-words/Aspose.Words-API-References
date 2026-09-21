---
title: "Aspose::Words::Saving::PageSavingArgs::get_PageStream metod"
linktitle: "get_PageStream"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PageSavingArgs::get_PageStream metod. Tillåter att ange strömmen där dokumentsidan sparas i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Tillåter att ange strömmen där dokumentsidan kommer att sparas.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Anmärkningar


Denna egenskap tillåter dig att spara dokumentsidor till strömmar istället för filer.

Standardvärdet är **null**. När denna egenskap är **null** kommer dokumentsidan att sparas till en fil som anges i egenskapen [PageFileName](../get_pagefilename/).

Om både [PageStream](./) och [PageFileName](../get_pagefilename/) är angivna, kommer PageStream att användas.

## Se även

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
