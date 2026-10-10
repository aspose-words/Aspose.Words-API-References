---
title: "Aspose::Words::BuildVersionInfo class"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BuildVersionInfo class. Tillhandahåller information om det aktuella produktnamnet och versionen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Tillhandahåller information om det aktuella produktnamnet och versionen. För att läsa mer, besök dokumentationsartikeln [Generator‑ eller producentnamn som inkluderas i utdata‑dokument](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Hämtar produktens fullständiga namn. |
| static [get_Version](./get_version/)() | Hämtar produktens version. |

## Exempel



Visar hur man visar information om din installerade version av Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
