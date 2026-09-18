---
title: "Aspose::Words::TextColumnCollection::get_Spacing Methode"
linktitle: "get_Spacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumnCollection::get_Spacing Methode. Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten in C++ abgerufen oder festgelegt."
type: docs
weight: 5000
url: /de/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten ermittelt oder festgelegt.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
