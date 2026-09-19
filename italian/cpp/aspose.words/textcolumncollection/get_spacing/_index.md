---
title: "Aspose::Words::TextColumnCollection::get_Spacing metodo"
linktitle: "get_Spacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumnCollection::get_Spacing metodo. Quando le colonne sono equamente distanziate, ottiene o imposta la quantità di spazio tra ogni colonna in punti in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


Quando le colonne sono equidistanti, ottiene o imposta la quantità di spazio tra ogni colonna in punti.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
