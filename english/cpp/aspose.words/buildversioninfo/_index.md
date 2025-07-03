---
title: Aspose::Words::BuildVersionInfo class
linktitle: BuildVersionInfo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildVersionInfo class. Provides information about the current product name and version. To learn more, visit the  documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Provides information about the current product name and version. To learn more, visit the [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/) documentation article.

```cpp
class BuildVersionInfo
```

## Methods

| Method | Description |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Gets the full name of the product. |
| static [get_Version](./get_version/)() | Gets the product version. |

## Examples



Shows how to display information about your installed version of Aspose.Words. 
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
