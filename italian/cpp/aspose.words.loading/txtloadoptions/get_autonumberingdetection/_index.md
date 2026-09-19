---
title: "Metodo Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection"
linktitle: "get_AutoNumberingDetection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection. Ottiene o imposta un valore booleano che indica se il rilevamento automatico della numerazione verrà eseguito durante il caricamento di un documento. Il valore predefinito è true in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Ottiene o imposta un valore booleano che indica se verrà eseguita la rilevazione automatica della numerazione durante il caricamento di un documento. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Esempi



Mostra come disabilitare il rilevamento automatico della numerazione.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## Vedi anche

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
