---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns metodo"
linktitle: "get_Columns"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns metodo. Specifica il numero di colonne con cui l'area delle note a piè di pagina è formattata in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Specifica il numero di colonne con cui l'area delle note a piè di pagina è formattata.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Esempi



Mostra come suddividere la sezione delle note a piè di pagina in un determinato numero di colonne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## Vedi anche

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
