---
title: "Aspose::Words::BuildVersionInfo::get_Version metod"
linktitle: "get_Version"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BuildVersionInfo::get_Version metod. Hämtar produktens version i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Hämtar produktens version.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Anmärkningar


Produktversionen är i formatet "Major.Minor.Hotfix.0".

## Exempel



Visar hur man visar information om din installerade version av Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Se även

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
