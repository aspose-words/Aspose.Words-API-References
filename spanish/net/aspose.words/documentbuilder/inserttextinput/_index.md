---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words para .NET
description: Añade fácilmente campos de texto en el formulario con el método InsertTextInput de DocumentBuilder. ¡Mejora la interactividad y la experiencia de usuario de tus documentos hoy mismo!
type: docs
weight: 510
url: /es/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Inserta un campo de formulario de texto en la posición actual.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre del campo de formulario. Puede ser una cadena vacía. |
| type | TextFormFieldType | Especifica el tipo de campo de formulario de texto. |
| format | String | Cadena de formato utilizada para formatear el valor del campo de formulario. |
| fieldValue | String | Texto que se mostrará en el campo. |
| maxLength | Int32 | Longitud máxima que el usuario puede introducir en el campo del formulario. Se establece en cero para una longitud ilimitada. |

### Valor_devuelto

El nodo del campo de formulario que se acaba de insertar.

## Observaciones

Si especifica un nombre para el campo de formulario, se creará automáticamente un marcador con el mismo nombre.

## Ejemplos

Muestra cómo insertar un campo de formulario de entrada de texto en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un formulario que solicita al usuario que ingrese texto.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Muestra cómo insertar un campo de formulario de entrada de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Inserte un campo de entrada de texto, que permitirá al usuario hacer clic en él e ingresar texto.
// Asignar un texto de marcador de posición que el usuario pueda sobrescribir y pasar
// una longitud de texto máxima de 0 para no aplicar ningún límite al contenido del campo de formulario.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// El campo de formulario aparecerá en forma de una etiqueta html "input", con un tipo de "texto".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
