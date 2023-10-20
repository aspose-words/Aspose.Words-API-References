---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words para .NET
description: DocumentBuilder InsertTextInput método. Inserta un campo de formulario de texto en la posición actual en C#.
type: docs
weight: 470
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
| name | String | El nombre del campo del formulario. Puede ser una cadena vacía. |
| type | TextFormFieldType | Especifica el tipo de campo de formulario de texto. |
| format | String | Cadena de formato utilizada para formatear el valor del campo del formulario. |
| fieldValue | String | Texto que se mostrará en el campo. |
| maxLength | Int32 | Longitud máxima que el usuario puede ingresar en el campo del formulario. Establezca en cero para una duración ilimitada. |

### Valor_devuelto

El nodo del campo de formulario que se acaba de insertar.

## Observaciones

Si especifica un nombre para el campo del formulario, se crea automáticamente un marcador con el mismo nombre.

## Ejemplos

Muestra cómo insertar un campo de formulario de entrada de texto en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un formulario que solicite al usuario que ingrese texto.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Muestra cómo insertar un campo de formulario de entrada de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Inserta un campo de entrada de texto, que permitirá al usuario hacer clic en él e ingresar texto.
// Asigna un texto de marcador de posición que el usuario puede sobrescribir y pasar
// una longitud máxima de texto de 0 para no aplicar ningún límite al contenido del campo del formulario.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// El campo del formulario aparecerá en forma de etiqueta html de "entrada", con un tipo de "texto".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

Muestra cómo crear campos de formulario.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Los campos de formulario son objetos en el documento con los que el usuario puede interactuar al solicitarle que ingrese valores.
// Podemos crearlos usando un generador de documentos y a continuación se muestran dos formas de hacerlo.
// 1 - Entrada de texto básico:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Cuadro combinado con texto emergente y un rango de valores posibles:
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
