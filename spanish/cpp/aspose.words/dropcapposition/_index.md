---
title: "Aspose::Words::DropCapPosition enumeración"
linktitle: "DropCapPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DropCapPosition enumeración. Especifica la posición para un texto con letra capitular en C++."
type: docs
weight: 87000
url: /es/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Especifica la posición del texto de letra capitular.

```cpp
enum class DropCapPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | El párrafo no tiene una letra capitular. |
| Normal | 1 | La letra capitular está posicionada dentro del margen del texto en el párrafo ancla. |
| Margen | 2 | La letra capitular está posicionada fuera del margen del texto en el párrafo ancla. |


## Ejemplos



Muestra cómo crear una letra capitular.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un párrafo con una letra grande con la que comienza el texto en los párrafos segundo y tercero.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actualmente, los párrafos segundo y tercero aparecerán debajo del primero.
// Podemos convertir el primer párrafo en una letra capitular para los demás párrafos mediante su objeto "ParagraphFormat".
// Establezca la propiedad "DropCapPosition" a "DropCapPosition.Margin" para colocar la letra capitular
// fuera del margen izquierdo de la página si nuestro texto es de izquierda a derecha.
// Establezca la propiedad "DropCapPosition" a "DropCapPosition.Normal" para colocar la letra capitular dentro de los márgenes de la página
// y para que el resto del texto fluya a su alrededor.
// "DropCapPosition.None" es el estado predeterminado para todos los párrafos.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
