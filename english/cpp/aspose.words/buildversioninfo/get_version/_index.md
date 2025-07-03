---
title: Aspose::Words::BuildVersionInfo::get_Version method
linktitle: get_Version
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildVersionInfo::get_Version method. Gets the product version in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Gets the product version.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Remarks


The product version is in the "Major.Minor.Hotfix.0" format.

## Examples



Shows how to display information about your installed version of Aspose.Words. 
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## See Also

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
