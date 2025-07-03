---
title: Aspose::Words::BuildVersionInfo::get_Product method
linktitle: get_Product
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildVersionInfo::get_Product method. Gets the full name of the product in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Gets the full name of the product.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Examples



Shows how to display information about your installed version of Aspose.Words. 
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## See Also

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
