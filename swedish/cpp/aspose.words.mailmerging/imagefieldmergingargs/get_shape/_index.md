---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape metod"
linktitle: "get_Shape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape metod. Anger formen som mail‑sammanfognings‑motorn måste infoga i dokumentet i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Anger formen som mail merge‑motorn måste infoga i dokumentet.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Anmärkningar


När den här egenskapen anges ignorerar mail‑sammanfognings‑motorn alla andra egenskaper som [ImageFileName](../get_imagefilename/) eller [ImageStream](../get_imagestream/) och infogar helt enkelt formen i dokumentet.

Använd den här egenskapen för att fullt kontrollera processen för att slå samman ett bildsammanfogningsfält. Till exempel kan du ange [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) eller någon annan form‑egenskap för att finjustera den resulterande noden. Observera dock att du är ansvarig för att tillhandahålla innehållet i formen.
## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
