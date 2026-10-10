---
title: "Aspose::Words::DocumentBuilder::Writeln Methode"
linktitle: "Writeln"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::Writeln Methode. Fügt einen Absatzumbruch in das Dokument in C++ ein."
type: docs
weight: 73000
url: /de/cpp/aspose.words/documentbuilder/writeln/
---
## DocumentBuilder::Writeln() method


Fügt einen Absatzumbruch in das Dokument ein.

```cpp
void Aspose::Words::DocumentBuilder::Writeln()
```

## Hinweise


Ruft [InsertParagraph](../insertparagraph/) auf.
## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::Writeln(const System::String\&) method


Fügt eine Zeichenkette und einen Absatzumbruch in das Dokument ein.

```cpp
void Aspose::Words::DocumentBuilder::Writeln(const System::String &text)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | const System::String\& | Die Zeichenkette, die in das Dokument eingefügt werden soll. |

## Beispiele



Zeigt, wie man eine formatierte 2x2‑Tabelle erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Während der Erstellung der Tabelle wendet der Document Builder seine aktuellen RowFormat/CellFormat‑Eigenschaftswerte an
// auf die aktuelle Zeile/Zelle, in der sich der Cursor befindet, und auf alle neuen Zeilen/Zellen, die er erstellt.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Zuvor hinzugefügte Zeilen und Zellen werden nicht rückwirkend von Änderungen der Formatierung des Builders beeinflusst.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
