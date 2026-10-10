---
title: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection yöntemi"
linktitle: "get_AutoNumberingDetection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection yöntemi. Bir belge yüklenirken otomatik numaralandırma algılamasının yapılacağını gösteren bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta true'dır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


Bir belge yüklenirken otomatik numaralandırma algılamasının yapılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## Örnekler



Otomatik numaralandırma algılamasını nasıl devre dışı bırakılacağını gösterir.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## Ayrıca Bakınız

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
