---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected metodo"
linktitle: "get_IsProtected"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected metodo. Mostra se il VbaProject è protetto da password in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


Mostra se il [VbaProject](../) è protetto da password.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Esempi



Mostra se il [VbaProject](../) è protetto da password.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## Vedi anche

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
