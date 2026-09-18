---
title: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection Methode"
linktitle: "get_AutoNumberingDetection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection Methode. Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob die automatische Nummerierungserkennung beim Laden eines Dokuments durchgeführt wird. Der Standardwert ist true in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Liest oder setzt einen booleschen Wert, der angibt, ob die automatische Nummerierungserkennung beim Laden eines Dokuments durchgeführt wird. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Beispiele



Zeigt, wie die automatische Nummerierungserkennung deaktiviert wird.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## Siehe auch

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
