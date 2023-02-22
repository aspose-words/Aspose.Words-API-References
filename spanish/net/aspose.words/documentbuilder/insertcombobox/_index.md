---
title: DocumentBuilder.InsertComboBox
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta un campo de formulario de cuadro combinado en la posición actual.
type: docs
weight: 280
url: /es/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Inserta un campo de formulario de cuadro combinado en la posición actual.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre del campo de formulario. Puede ser una cadena vacía. El valor de más de 20 caracteres se truncará. |
| items | String[] | Los elementos del ComboBox. El máximo es de 25 artículos. |
| selectedIndex | Int32 | El índice del elemento seleccionado en el ComboBox. |

### Valor_devuelto

El nodo de campo de formulario que se acaba de insertar.

### Observaciones

Si especifica un nombre para el campo de formulario, se crea automáticamente un marcador con el mismo nombre.

### Ejemplos

Muestra cómo insertar un campo de formulario de cuadro combinado en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un formulario que solicite al usuario que elija uno de los elementos del menú.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Muestra cómo crear campos de formulario.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Los campos de formulario son objetos en el documento con los que el usuario puede interactuar si se le solicita que ingrese valores.
// Podemos crearlos usando un generador de documentos, ya continuación hay dos formas de hacerlo.
// 1 - Entrada de texto básico:
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
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


