---
title: "Método Aspose::Words::Border::get_Shadow"
linktitle: "get_Shadow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Border::get_Shadow. Obtiene o establece un valor que indica si el borde tiene sombra en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Obtiene o establece un valor que indica si el borde tiene sombra.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Observaciones


En Microsoft Word, para que un borde tenga sombra, los bordes en los cuatro lados (izquierda, superior, derecha e inferior) deben ser del mismo tipo, ancho, color y todos deben tener la propiedad Shadow establecida en **true**.

## Ejemplos



Muestra cómo crear un borde de página ondulado verde con una sombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## Ver también

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
