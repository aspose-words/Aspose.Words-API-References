---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns метод"
linktitle: "get_Columns"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns метод. Указывает количество столбцов, с которыми форматируется область сносок в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Указывает количество колонок, в которых форматируется область сносок.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Примеры



Показывает, как разделить раздел сносок на заданное количество колонок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## См. также

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
