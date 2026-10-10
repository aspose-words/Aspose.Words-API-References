---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns metod"
linktitle: "get_Columns"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns metod. Anger antalet kolumner som fotnotområdet formateras med i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Anger antalet kolumner som fotnotområdet formateras med.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Exempel



Visar hur man delar fotnotsektionen i ett givet antal kolumner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## Se även

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
