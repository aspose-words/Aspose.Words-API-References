---
title: "Aspose::Words::Rendering::PageInfo::get_Colored-Methode"
linktitle: "get_Colored"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::PageInfo::get_Colored-Methode. Gibt true zurück, wenn die Seite farbige Inhalte enthält, in C++."
type: docs
weight: 1500
url: /de/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Gibt **true** zurück, wenn die Seite farbigen Inhalt enthält.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Beispiele



Zeigt, wie geprüft wird, ob die Seite farbig ist oder nicht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Überprüfen Sie, dass die erste Seite des Dokuments nicht farbig ist.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Siehe auch

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
