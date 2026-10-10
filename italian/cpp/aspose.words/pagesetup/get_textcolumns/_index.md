---
title: "Aspose::Words::PageSetup::get_TextColumns metodo"
linktitle: "get_TextColumns"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_TextColumns metodo. Restituisce una collezione che rappresenta l'insieme delle colonne di testo in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


Restituisce una raccolta che rappresenta l'insieme delle colonne di testo.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
```


## Esempi



Mostra come creare più colonne equidistanti in una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Vedi anche

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
