---
title: "Aspose::Words::BuildVersionInfo sınıfı"
linktitle: "BuildVersionInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildVersionInfo sınıfı. Mevcut ürün adı ve sürümü hakkında bilgi sağlar. Daha fazla bilgi edinmek için C++'daki belgeler makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Mevcut ürün adı ve sürümü hakkında bilgi sağlar. Daha fazla bilgi için, [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class BuildVersionInfo
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Ürünün tam adını alır. |
| static [get_Version](./get_version/)() | Ürün sürümünü alır. |

## Örnekler



Yüklü Aspose.Words sürümünüz hakkında bilgiyi nasıl görüntüleyeceğinizi gösterir.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
