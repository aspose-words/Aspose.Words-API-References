---
title: "Aspose::Words::BorderCollection::get_Bottom Methode"
linktitle: "get_Bottom"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_Bottom Methode. Gibt den unteren Rahmen in C++ zurück."
type: docs
weight: 4000
url: /de/cpp/aspose.words/bordercollection/get_bottom/
---
## BorderCollection::get_Bottom method


Liefert den unteren Rahmen.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Bottom()
```


## Beispiele



Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Beginne eine Tabelle und lege eine Standardfarbe/Dicke für ihre Rahmen fest.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Erstelle eine Zeile mit zwei Zellen, die unterschiedliche Hintergrundfarben haben.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Setze die Zellenformatierung zurück, um die Hintergrundfarben zu deaktivieren
// setze eine benutzerdefinierte Rahmendicke für alle neuen Zellen, die vom Builder erstellt werden,
// und erstelle dann eine zweite Zeile.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```

## Siehe auch

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
