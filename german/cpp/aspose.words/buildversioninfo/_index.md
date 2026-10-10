---
title: "Aspose::Words::BuildVersionInfo class"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildVersionInfo class. Liefert Informationen über den aktuellen Produktnamen und die Version. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Stellt Informationen über den aktuellen Produktnamen und die Version bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Gibt den vollständigen Namen des Produkts zurück. |
| static [get_Version](./get_version/)() | Gibt die Produktversion zurück. |

## Beispiele



Zeigt, wie Informationen über Ihre installierte Version von Aspose.Words angezeigt werden.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
