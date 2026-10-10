---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected método"
linktitle: "get_IsProtected"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected método. Muestra si el VbaProject está protegido con contraseña en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


Muestra si el [VbaProject](../) está protegido con contraseña.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Ejemplos



Muestra si el [VbaProject](../) está protegido con contraseña.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## Ver también

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
