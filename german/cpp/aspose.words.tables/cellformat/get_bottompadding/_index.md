---
title: "Aspose::Words::Tables::CellFormat::get_BottomPadding Methode"
linktitle: "get_BottomPadding"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::get_BottomPadding Methode. Gibt die Menge an Raum (in Punkten) zurück oder legt sie fest, die unter dem Inhalt der Zelle in C++ hinzugefügt wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.tables/cellformat/get_bottompadding/
---
## CellFormat::get_BottomPadding method


Gibt die Menge des (in Punkten) hinzuzufügenden Abstands unter dem Zellinhalt zurück oder legt sie fest.

```cpp
double Aspose::Words::Tables::CellFormat::get_BottomPadding()
```


## Beispiele



Zeigt, wie man Zellen mit einem DocumentBuilder formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Fügen Sie eine zweite Zelle ein und konfigurieren Sie dann die Optionen für den Zelltext‑Abstand.
// Der Builder wendet diese Einstellungen auf seine aktuelle Zelle an, und alle danach erstellten neuen Zellen übernehmen sie.
builder->InsertCell();

System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = builder->get_CellFormat();
cellFormat->set_Width(250);
cellFormat->set_LeftPadding(30);
cellFormat->set_RightPadding(30);
cellFormat->set_TopPadding(30);
cellFormat->set_BottomPadding(30);

builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->EndTable();

// Die erste Zelle war von der Neukonfiguration des Abstands unbeeinflusst und behält weiterhin die Standardwerte.
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_BottomPadding());

ASPOSE_ASSERT_EQ(250.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_BottomPadding());

// Die erste Zelle wird im Ausgabedokument weiterhin wachsen, um die Größe der benachbarten Zelle anzupassen.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## Siehe auch

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
