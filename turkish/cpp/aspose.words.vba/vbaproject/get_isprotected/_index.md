---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected yöntemi"
linktitle: "get_IsProtected"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected yöntemi. C++'ta VbaProject'in şifre korumalı olup olmadığını gösterir."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


[VbaProject](../) öğesinin şifre korumalı olup olmadığını gösterir.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Örnekler



[VbaProject](../) öğesinin şifre korumalı olup olmadığını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## Ayrıca Bakınız

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
