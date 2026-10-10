---
title: "Aspose::Words::Paragraph::get_IsFormatRevision metod"
linktitle: "get_IsFormatRevision"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::get_IsFormatRevision metod. Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Returnerar true om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Exempel



Visar hur man kontrollerar om ett stycke är en formatrevision.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Detta stycke är en "Format"-revision, vilket sker när vi ändrar formateringen av befintlig text
// medan vi spårar revisioner i Microsoft Word via "Review" -> "Track changes".
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## Se även

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
