---
title: "Aspose::Words::Rendering::PageInfo::get_Colored yöntemi"
linktitle: "get_Colored"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::PageInfo::get_Colored yöntemi. Sayfa renkli içerik içeriyorsa C++'ta true döndürür."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Sayfa renkli içerik içeriyorsa **true** döndürür.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Örnekler



Sayfanın renkli olup olmadığını nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Belgenin ilk sayfasının renkli olmadığını kontrol edin.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Ayrıca Bakınız

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
