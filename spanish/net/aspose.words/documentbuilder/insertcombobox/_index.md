---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words para .NET
description: Mejore sus documentos con el método InsertComboBox de DocumentBuilder. Agregue fácilmente campos de formulario de cuadro combinado interactivos para una mejor experiencia de usuario.
type: docs
weight: 300
url: /es/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Inserta un campo de formulario de cuadro combinado en la posición actual.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre del campo del formulario. Puede ser una cadena vacía. Los valores con más de 20 caracteres se truncarán. |
| items | String[] | Elementos del ComboBox. Máximo de 25 elementos. |
| selectedIndex | Int32 | El índice del elemento seleccionado en el ComboBox. |

### Valor_devuelto

El nodo del campo de formulario que se acaba de insertar.

## Observaciones

Si especifica un nombre para el campo de formulario, se creará automáticamente un marcador con el mismo nombre.

## Ejemplos

Muestra cómo insertar un campo de formulario de cuadro combinado en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un formulario que solicita al usuario que elija uno de los elementos del menú.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
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
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
