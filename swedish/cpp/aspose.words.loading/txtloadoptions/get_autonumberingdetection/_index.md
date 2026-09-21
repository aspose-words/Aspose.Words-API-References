---
title: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection-metod"
linktitle: "get_AutoNumberingDetection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection-metod. Hämtar eller anger ett booleskt värde som visar om automatisk numreringsdetektering ska utföras vid inläsning av ett dokument. Standardvärdet är true i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Hämtar eller anger ett booleskt värde som indikerar om automatisk numreringsdetektering ska utföras vid inläsning av ett dokument. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Exempel



Visar hur man inaktiverar automatisk numreringsdetektering.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## Se även

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
