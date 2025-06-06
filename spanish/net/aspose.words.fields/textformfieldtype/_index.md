---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Fields.TextFormFieldType, que define varios tipos de campos de formulario de texto para una mejor automatización y personalización de documentos.
type: docs
weight: 3180
url: /es/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Especifica el tipo de un campo de formulario de texto.

```csharp
public enum TextFormFieldType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Regular | `0` | El campo de formulario de texto puede contener cualquier texto. |
| Number | `1` | El campo de formulario de texto solo puede contener números. |
| Date | `2` | El campo de formulario de texto solo puede contener un valor de fecha válido. |
| CurrentDate | `3` | El valor del campo de formulario de texto es la fecha actual en la que se actualiza el campo. |
| CurrentTime | `4` | El valor del campo de formulario de texto es la hora actual en que se actualiza el campo. |
| Calculated | `5` | El valor del campo de formulario de texto se calcula a partir de la expresión especificada en [`TextInputDefault`](../formfield/textinputdefault/) propiedad. |

## Ejemplos

Muestra cómo crear campos de formulario.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Los campos de formulario son objetos en el documento con los que el usuario puede interactuar al solicitarle que ingrese valores.
// Podemos crearlos usando un generador de documentos. A continuación se muestran dos formas de hacerlo.
// 1 - Entrada de texto básica:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Cuadro combinado con texto de solicitud y un rango de valores posibles:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
