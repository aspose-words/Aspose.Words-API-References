---
title: List.IsListStyleReference
linktitle: IsListStyleReference
articleTitle: IsListStyleReference
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsListStyleReference, que indica si una lista hace referencia a un estilo específico, mejorando el formato y la organización de su documento.
type: docs
weight: 30
url: /es/net/aspose.words.lists/list/isliststylereference/
---
## List.IsListStyleReference property

Devuelve`verdadero` si esta lista es una referencia a un estilo de lista.

```csharp
public bool IsListStyleReference { get; }
```

## Observaciones

Tenga en cuenta que modificar las propiedades de una lista que es una referencia al estilo de lista no tiene ningún efecto. El formato de lista especificado en el propio estilo de lista siempre tiene prioridad.

## Ejemplos

Muestra cómo crear un estilo de lista y usarlo en un documento.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
//Podemos contener un objeto Lista completo dentro de un estilo.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Cambiar la apariencia de todos los niveles de lista en nuestra lista.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Crea otra lista a partir de una lista dentro de un estilo.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Agregue algunos elementos de lista que nuestra lista formateará.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Crea y aplica otra lista basada en el estilo de lista.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Ver también

* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
