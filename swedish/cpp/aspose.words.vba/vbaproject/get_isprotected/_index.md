---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected‑metod"
linktitle: "get_IsProtected"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected‑metod. Visar om VbaProject är lösenordsskyddad i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


Visar om [VbaProject](../) är lösenordsskyddad.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Exempel



Visar om [VbaProject](../) är lösenordsskyddad.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## Se även

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
