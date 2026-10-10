---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns yöntemi"
linktitle: "get_Columns"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns yöntemi. C++'da dipnot alanının biçimlendirildiği sütun sayısını belirtir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Dipnot alanının biçimlendirildiği sütun sayısını belirtir.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Örnekler



Dipnot bölümünün belirli bir sütun sayısına bölünmesini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## Ayrıca Bakınız

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
