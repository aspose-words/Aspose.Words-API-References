---
title: "Método Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars"
linktitle: "get_ShowRevisionBars"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars. Permite especificar si las barras de revisión deben renderizarse cerca de las líneas que contienen contenido revisado. El valor predeterminado es true en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.layout/revisionoptions/get_showrevisionbars/
---
## RevisionOptions::get_ShowRevisionBars method


Permite especificar si las barras de revisión deben renderizarse cerca de las líneas que contienen contenido revisado. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars() const
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

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
