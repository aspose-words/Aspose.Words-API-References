---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::TextWrapping enum. Gibt an, wie Text um die Tabelle in C++ herumfließt."
type: docs
weight: 16000
url: /de/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Gibt an, wie Text um die Tabelle herumfließt.

```cpp
enum class TextWrapping
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Text und Tabelle werden in der Reihenfolge ihres Auftretens im Dokument angezeigt. |
| Um | 1 | Text wird um die Tabelle herumfließen und den verfügbaren Seitenraum einnehmen. |
| Standard | n/a | Standardwert. |


## Beispiele



Zeigt, wie man mit dem Textfluss um Tabellen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Setzen Sie die Eigenschaft "TextWrapping" auf "TextWrapping.Around", um die Tabelle dazu zu bringen, Text um sie herum zu fließen,
// und schieben Sie sie nach unten in den darunterliegenden Absatz, indem Sie die Position festlegen.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
