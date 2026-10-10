---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream metod"
linktitle: "get_ResourceStream"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream metod. Tillåter att ange den ström där resursen kommer att sparas i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Tillåter att ange strömmen där resursen ska sparas.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Anmärkningar


Denna egenskap låter dig spara resurser till strömmar istället för filer.

Standardvärdet är **null**. När denna egenskap är **null** kommer resursen att sparas till en fil som anges i egenskapen [ResourceFileName](../get_resourcefilename/).

Med hjälp av [IResourceSavingCallback](../../iresourcesavingcallback/) kan du inte ersätta en resurs med en annan. Det är endast avsett för att kontrollera var resurser ska sparas.

## Se även

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
