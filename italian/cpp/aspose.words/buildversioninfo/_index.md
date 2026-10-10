---
title: "classe Aspose::Words::BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::BuildVersionInfo. Fornisce informazioni sul nome e sulla versione attuali del prodotto. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Fornisce informazioni sul nome e sulla versione del prodotto corrente. Per saperne di più, visita l'articolo di documentazione [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Restituisce il nome completo del prodotto. |
| static [get_Version](./get_version/)() | Restituisce la versione del prodotto. |

## Esempi



Mostra come visualizzare le informazioni sulla versione installata di Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
