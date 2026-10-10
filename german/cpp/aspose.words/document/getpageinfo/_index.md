---
title: "Aspose::Words::Document::GetPageInfo Methode"
linktitle: "GetPageInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::GetPageInfo Methode. Ermittelt die Seitengröße, Ausrichtung und weitere Informationen über eine Seite, die für das Drucken oder Rendern in C++ nützlich sein können."
type: docs
weight: 62000
url: /de/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Liest die Seitengröße, Ausrichtung und weitere Informationen über eine Seite, die für den Druck oder das Rendern nützlich sein können.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | int32_t | Der 0-basierte Seitenindex. |

## Beispiele



Zeigt, wie geprüft wird, ob die Seite farbig ist oder nicht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Überprüfen Sie, dass die erste Seite des Dokuments nicht farbig ist.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Siehe auch

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
