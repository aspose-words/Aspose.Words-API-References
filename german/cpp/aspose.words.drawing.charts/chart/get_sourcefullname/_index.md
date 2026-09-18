---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName Methode"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName Methode. Gibt den Pfad und Namen einer xls/xlsx-Datei zurück, mit der dieses Diagramm in C++ verknüpft ist."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Ermittelt den Pfad und Namen einer xls/xlsx-Datei, mit der dieses Diagramm verknüpft ist.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Beispiele



Zeigt, wie man den vollständigen Namen des externen xls/xlsx-Dokuments abruft/setzt, wenn das Diagramm verknüpft ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## Siehe auch

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
