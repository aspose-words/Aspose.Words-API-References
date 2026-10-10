---
title: "Aspose::Words::Font::get_Scaling método"
linktitle: "get_Scaling"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_Scaling método. Obtiene o establece el escalado del ancho de caracteres en porcentaje en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Obtiene o establece la escala de ancho de carácter en porcentaje.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
```


## Ejemplos



Muestra cómo establecer el escalado horizontal y el espaciado para los caracteres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega una secuencia de texto y aumenta el ancho de los caracteres al 150%.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Agrega una secuencia de texto y añade 1 pt de espaciado horizontal extra entre cada carácter.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Agrega una secuencia de texto y acerca los caracteres entre sí en 1 pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
