---
title: "Aspose::Words::BuildVersionInfo::get_Product metodo"
linktitle: "get_Product"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildVersionInfo::get_Product metodo. Ottiene il nome completo del prodotto in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Restituisce il nome completo del prodotto.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Esempi



Mostra come visualizzare le informazioni sulla versione installata di Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Vedi anche

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
