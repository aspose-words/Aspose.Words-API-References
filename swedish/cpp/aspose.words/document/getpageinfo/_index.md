---
title: "Aspose::Words::Document::GetPageInfo metod"
linktitle: "GetPageInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::GetPageInfo metod. Hämtar sidstorlek, orientering och annan information om en sida som kan vara användbar för utskrift eller rendering i C++."
type: docs
weight: 62000
url: /sv/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Hämtar sidstorlek, orientering och annan information om en sida som kan vara användbar för utskrift eller rendering.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | int32_t | Det 0‑baserade sidindexet. |

## Exempel



Visar hur man kontrollerar om sidan är i färg eller inte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Kontrollera att den första sidan i dokumentet inte är färgad.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Se även

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
