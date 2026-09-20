---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected метод"
linktitle: "get_IsProtected"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected метод. Показывает, защищён ли VbaProject паролем в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


Показывает, защищён ли [VbaProject](../) паролем.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Примеры



Показывает, защищён ли [VbaProject](../) паролем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## См. также

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
