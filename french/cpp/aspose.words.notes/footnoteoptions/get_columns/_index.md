---
title: "Méthode Aspose::Words::Notes::FootnoteOptions::get_Columns"
linktitle: "get_Columns"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Notes::FootnoteOptions::get_Columns. Spécifie le nombre de colonnes avec lesquelles la zone des notes de bas de page est formatée en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


Spécifie le nombre de colonnes avec lesquelles la zone des notes de bas de page est formatée.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## Exemples



Montre comment diviser la section des notes de bas de page en un nombre donné de colonnes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## Voir aussi

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
