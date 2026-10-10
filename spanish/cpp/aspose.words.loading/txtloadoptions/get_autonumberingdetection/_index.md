---
title: "Método Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection"
linktitle: "get_AutoNumberingDetection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection. Obtiene o establece un valor booleano que indica si se realizará la detección automática de numeración al cargar un documento. El valor predeterminado es true en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Obtiene o establece un valor booleano que indica si se realizará la detección automática de numeración al cargar un documento. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Ejemplos



Muestra cómo desactivar la detección automática de numeración.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## Ver también

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
