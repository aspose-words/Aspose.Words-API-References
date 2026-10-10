---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream‑metod"
linktitle: "get_ImageStream"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream‑metod. Tillåter att ange strömmen där bilden ska sparas i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Tillåter att ange strömmen där bilden ska sparas till.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Anmärkningar


Denna egenskap låter dig spara bilder till strömmar istället för filer under HTML.

Standardvärdet är **null**. När denna egenskap är **null** sparas bilden till en fil som anges i egenskapen [ImageFileName](../get_imagefilename/).

Med [IImageSavingCallback](../../iimagesavingcallback/) kan du inte ersätta en bild med en annan. Den är avsedd endast för kontroll över var bilder ska sparas.

## Se även

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
