---
title: "Aspose::Words::PageSetup::get_TextColumns Methode"
linktitle: "get_TextColumns"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_TextColumns Methode. Gibt eine Sammlung zurück, die die Menge der Textspalten darstellt, in C++."
type: docs
weight: 44000
url: /de/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


Gibt eine Sammlung zurück, die die Menge der Textspalten darstellt.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
```


## Beispiele



Zeigt, wie man mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellt.
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

## Siehe auch

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
