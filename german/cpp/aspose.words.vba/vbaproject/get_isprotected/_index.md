---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected Methode"
linktitle: "get_IsProtected"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected Methode. Zeigt, ob das VbaProject in C++ passwortgeschützt ist."
type: docs
weight: 4500
url: /de/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


Zeigt, ob das [VbaProject](../) passwortgeschützt ist.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## Beispiele



Zeigt, ob das [VbaProject](../) passwortgeschützt ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## Siehe auch

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
