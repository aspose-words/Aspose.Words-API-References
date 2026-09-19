---
title: "Aspose::Words::TextColumnCollection::get_Count metodo"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumnCollection::get_Count metodo. Ottiene il numero di colonne nella sezione di un documento in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Restituisce il numero di colonne nella sezione di un documento.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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
