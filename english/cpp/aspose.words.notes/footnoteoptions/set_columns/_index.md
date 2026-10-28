---
title: Aspose::Words::Notes::FootnoteOptions::set_Columns method
linktitle: set_Columns
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteOptions::set_Columns method. Specifies the number of columns with which the footnotes area is formatted in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.notes/footnoteoptions/set_columns/
---
## FootnoteOptions::set_Columns method


Specifies the number of columns with which the footnotes area is formatted.

```cpp
void Aspose::Words::Notes::FootnoteOptions::set_Columns(int32_t value)
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
