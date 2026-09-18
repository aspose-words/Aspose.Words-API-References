---
title: "Aspose::Words::TextColumnCollection::get_Count Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumnCollection::get_Count Methode. Gibt die Anzahl der Spalten im Abschnitt eines Dokuments in C++ zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Ermittelt die Anzahl der Spalten im Abschnitt eines Dokuments.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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
