---
title: "Aspose::Words::BuildVersionInfo::get_Version Methode"
linktitle: "get_Version"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildVersionInfo::get_Version method. Gibt die Produktversion in C++ zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Gibt die Produktversion zurück.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Hinweise


Die Produktversion hat das Format "Major.Minor.Hotfix.0".

## Beispiele



Zeigt, wie Informationen über Ihre installierte Version von Aspose.Words angezeigt werden.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Siehe auch

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
