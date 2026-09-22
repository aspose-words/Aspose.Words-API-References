---
title: "Aspose::Words::BuildVersionInfo::get_Version metodu"
linktitle: "get_Version"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildVersionInfo::get_Version metodu. C++'da ürün sürümünü alır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Ürün sürümünü alır.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Açıklamalar


Ürün sürümü "Major.Minor.Hotfix.0" biçimindedir.

## Örnekler



Yüklü Aspose.Words sürümünüz hakkında bilgiyi nasıl görüntüleyeceğinizi gösterir.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Ayrıca Bakınız

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
