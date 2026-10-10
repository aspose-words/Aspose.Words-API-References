---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape método"
linktitle: "get_DisplayBackgroundShape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape método. Controla la visualización de la forma de fondo en la vista de diseño de impresión en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Controla la visualización de la forma de fondo en la vista de diseño de impresión.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Ejemplos



Muestra cómo ocultar/mostrar imágenes de fondo del documento en las opciones de vista.
```cpp
// Utilice una cadena HTML para crear un nuevo documento con un color de fondo plano.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// El origen del documento tiene un fondo de color plano,
// cuya presencia establecerá la bandera "DisplayBackgroundShape" a "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Mantenga la "DisplayBackgroundShape" como "true" para que el documento muestre el color de fondo.
// Esto puede afectar algunos colores de texto para mejorar la visibilidad.
// Establezca la "DisplayBackgroundShape" a "false" para no mostrar el color de fondo.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## Ver también

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
