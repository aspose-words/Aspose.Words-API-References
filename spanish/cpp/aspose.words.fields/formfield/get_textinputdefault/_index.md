---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault método"
linktitle: "get_TextInputDefault"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault método. Obtiene o establece la cadena predeterminada o una expresión de cálculo de un campo de formulario de texto en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Obtiene o establece la cadena predeterminada o una expresión de cálculo de un campo de formulario de texto.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Observaciones


El significado de esta propiedad depende del valor de la propiedad [TextInputType](../get_textinputtype/).

Cuando [TextInputType](../get_textinputtype/) es [Regular](../../textformfieldtype/) o [Number](../../textformfieldtype/), esta cadena especifica la cadena predeterminada para el campo de formulario de texto. Esta cadena es el contenido que Microsoft Word mostrará en el documento cuando el campo de formulario esté vacío.

Cuando [TextInputType](../get_textinputtype/) es [Calculated](../../textformfieldtype/), esta cadena contiene la expresión a calcular. La expresión debe ser una fórmula válida según los requisitos de los campos de fórmula de Microsoft Word. Cuando estableces una nueva expresión usando esta propiedad, Aspose.Words calcula el resultado de la fórmula automáticamente y lo inserta en el campo de formulario.

Microsoft Word permite cadenas con un máximo de 255 caracteres.
## Ver también

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
