---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns Methode"
linktitle: "get_Columns"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns Methode. Gibt die Anzahl der Spalten an, mit denen der Fußnotenbereich in C++ formatiert wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Gibt die Anzahl der Spalten an, mit denen der Fußnotenbereich formatiert wird.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Beispiele



Zeigt, wie man den Fußnotenabschnitt in eine gegebene Anzahl von Spalten aufteilt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## Siehe auch

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
