---
title: "Aspose::Words::BuildVersionInfo::get_Version metodo"
linktitle: "get_Version"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildVersionInfo::get_Version metodo. Ottiene la versione del prodotto in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Restituisce la versione del prodotto.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Note


La versione del prodotto è nel formato "Major.Minor.Hotfix.0".

## Esempi



Mostra come visualizzare le informazioni sulla versione installata di Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Vedi anche

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
