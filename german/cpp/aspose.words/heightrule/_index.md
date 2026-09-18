---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeightRule enum. Gibt die Regel zur Bestimmung der Höhe eines Objekts in C++ an."
type: docs
weight: 91000
url: /de/cpp/aspose.words/heightrule/
---
## HeightRule enum


Gibt die Regel zur Bestimmung der Höhe eines Objekts an.

```cpp
enum class HeightRule
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AtLeast | 0 | Die Höhe beträgt mindestens die angegebene Höhe in Punkten. Sie wächst bei Bedarf, um den gesamten Text im Objekt aufzunehmen. |
| Exactly | 1 | Die Höhe wird exakt in Punkten angegeben. Bitte beachten Sie, dass der Text abgeschnitten wird, wenn er nicht in das Objekt dieser Höhe passt. |
| Auto | 2 | Die Höhe wächst automatisch, um den gesamten Text im Objekt aufzunehmen. |


## Beispiele



Zeigt, wie man Zeilen mit einem Document Builder formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Starten Sie eine zweite Zeile und konfigurieren Sie anschließend deren Höhe. Der Builder wendet diese Einstellungen auf
// die aktuelle Zeile sowie auf alle neuen Zeilen an, die er danach erstellt.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// Die erste Zeile war von der Neupositionierung des Innenabstands nicht betroffen und behält weiterhin die Standardwerte.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
