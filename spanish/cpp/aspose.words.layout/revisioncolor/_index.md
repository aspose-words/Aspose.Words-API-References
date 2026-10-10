---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::RevisionColor enum. Permite especificar el color de las revisiones del documento en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Permite especificar el color de las revisiones del documento.

```cpp
enum class RevisionColor
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | 0 | Predeterminado. |
| Negro | 1 | Representa el color 000000. |
| Azul | 2 | Representa el color 2e97d3. |
| BrightGreen | 3 | Representa el color 84a35b. |
| ClassicBlue | 4 | Representa el color 0000ff. |
| ClassicRed | 5 | Representa el color ff0000. |
| DarkBlue | 6 | Representa el color 376e96. |
| DarkRed | 7 | Representa el color 881824. |
| DarkYellow | 8 | Representa el color e09a2b. |
| Gray25 | 9 | Representa el color a0a3a9. |
| Gray50 | 10 | Representa el color 50565e. |
| Green | 11 | Representa el color 2c6234. |
| Pink | 12 | Representa el color ce338f. |
| Red | 13 | Representa el color b5082e. |
| Teal | 14 | Representa el color 1b9cab. |
| Turquoise | 15 | Representa el color 3eafc2. |
| Violet | 16 | Representa el color 633277. |
| White | 17 | Representa el color ffffff. |
| Yellow | 18 | Representa el color fad272. |
| LightPink | 19 | Representa el color fce6f4. |
| LightBlue | 20 | Representa el color e1f2fa. |
| LightYellow | 21 | Representa el color fef4de. |
| LightPurple | 22 | Representa el color eadfef. |
| LightOrange | 23 | Representa el color fce3d0. |
| LightGreen | 24 | Representa el color e9f8ce. |
| Gray | 25 | Representa el color efeded. |
| NoHighlight | 26 | No se usa color para resaltar los cambios de revisión. |
| ByAuthor | 27 | Las revisiones de cada autor reciben su propio color para resaltar, de un conjunto predefinido de colores de alto contraste. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
