---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable‑metod"
linktitle: "get_IsImageAvailable"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable‑metod. Returnerar true om den aktuella bilden är tillgänglig för export i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Returnerar **true** om den aktuella bilden är tillgänglig för export.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Anmärkningar


Vissa bilder i dokumentet kan vara otillgängliga, till exempel eftersom bilden är länkad och länken är oåtkomlig eller inte pekar på en giltig bild. I så fall exporterar Aspose.Words en ikon med ett rött kryss. Denna egenskap returnerar **true** om den ursprungliga bilden är tillgänglig; returnerar **false** om den ursprungliga bilden inte är tillgänglig och en "ingen bild"-ikon kommer att erbjudas för sparning.

När en gruppform eller en form som inte kräver någon bild sparas är denna egenskap alltid **true**.

## Se även

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
