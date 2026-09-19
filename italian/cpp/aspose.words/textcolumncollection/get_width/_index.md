---
title: "Aspose::Words::TextColumnCollection::get_Width metodo"
linktitle: "get_Width"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumnCollection::get_Width metodo. Quando le colonne sono equamente distanziate, ottiene la larghezza delle colonne in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/textcolumncollection/get_width/
---
## TextColumnCollection::get_Width method


Quando le colonne sono equidistanti, ottiene la larghezza delle colonne.

```cpp
double Aspose::Words::TextColumnCollection::get_Width()
```

## Note


Ha effetto solo quando [EvenlySpaced](../get_evenlyspaced/) è impostato su **true**.

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
