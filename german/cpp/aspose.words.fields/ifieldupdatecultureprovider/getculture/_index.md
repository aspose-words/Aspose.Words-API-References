---
title: "Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture Methode"
linktitle: "GetCulture"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture Methode. Gibt ein CultureInfo-Objekt zurück, das während der Aktualisierung des Feldes in C++ verwendet wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


Gibt ein **CultureInfo**-Objekt zurück, das während der Aktualisierung des Feldes verwendet werden soll.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Kultur | System::String | Der Name der für das zu aktualisierende Feld angeforderten Kultur. |
| field | System::SharedPtr\<Aspose::Words::Fields::Field\> | Das zu aktualisierende Feld. |

### ReturnValue

Das Kulturobjekt, das für die Aktualisierung des Feldes verwendet werden soll.

## Siehe auch

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
