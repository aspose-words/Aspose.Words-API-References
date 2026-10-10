---
title: "Aspose::Words::Tables::Table::get_TopPadding-Methode"
linktitle: "get_TopPadding"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_TopPadding-Methode. Ruft die Menge des Abstandes (in Punkt) ab oder legt sie fest, die über dem Inhalt der Zellen in C++ hinzugefügt wird."
type: docs
weight: 40000
url: /de/cpp/aspose.words.tables/table/get_toppadding/
---
## Table::get_TopPadding method


Liest oder legt die Menge an Abstand (in Punkten) fest, die über dem Inhalt von Zellen hinzugefügt wird.

```cpp
double Aspose::Words::Tables::Table::get_TopPadding()
```


## Beispiele



Zeigt, wie man den Inhaltsabstand in einer Tabelle konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// Für jede Zelle in der Tabelle setzen Sie den Abstand zwischen ihrem Inhalt und jedem ihrer Ränder.
// Diese Tabelle behält den minimalen Abstand bei, indem sie den Text umbricht.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
