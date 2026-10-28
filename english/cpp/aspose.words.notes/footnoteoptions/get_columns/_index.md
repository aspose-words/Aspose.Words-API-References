---
title: Aspose::Words::Notes::FootnoteOptions::get_Columns method
linktitle: get_Columns
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteOptions::get_Columns method. Specifies the number of columns with which the footnotes area is formatted in C++.'
type: docs
weight: 8286
url: /cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Specifies the number of columns with which the footnotes area is formatted.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```

## Remarks

 If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0. 
## Examples


Shows how to split the footnote section into a given number of columns.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Footnotes and endnotes.docx"));

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```
## See Also

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
