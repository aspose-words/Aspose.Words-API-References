---
title: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition método"
linktitle: "get_RevisionBarsPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition método. Obtiene o establece la posición de renderizado de las barras de revisión. El valor predeterminado es Exterior en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


Obtiene o establece la posición de renderizado de las barras de revisión. El valor predeterminado es [Exterior](../../../aspose.words.drawing/horizontalalignment/).

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
```


## Ejemplos



Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Elimine la barra que aparece a la izquierda de cada línea revisada.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ver también

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
