---
title: "Enumeración Aspose::Words::Underline"
linktitle: "Subrayado"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Underline. Indica el tipo de subrayado aplicado a una fuente en C++."
type: docs
weight: 126000
url: /es/cpp/aspose.words/underline/
---
## Underline enum


Indica el tipo de subrayado aplicado a una fuente.

```cpp
enum class Underline
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 |  |
| Single | 1 |  |
| Words | 2 |  |
| Double | 3 |  |
| Dotted | 4 |  |
| Thick | 6 |  |
| Dash | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


## Ejemplos



Muestra cómo insertar un campo de hipervínculo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto clicable que nos llevará a la ubicación especificada en la URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL mediante una nueva ventana del navegador web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
