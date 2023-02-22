---
title: Enum StyleType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.StyleType enumeración. Representa el tipo del estilo.
type: docs
weight: 5860
url: /es/net/aspose.words/styletype/
---
## StyleType enumeration

Representa el tipo del estilo.

```csharp
public enum StyleType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Paragraph | `1` | El estilo es un estilo de párrafo. |
| Character | `2` | El estilo es un estilo de carácter. |
| Table | `3` | El estilo es un estilo de tabla. |
| List | `4` | El estilo es un estilo de lista. |

### Ejemplos

Muestra cómo crear un estilo de lista y usarlo en un documento.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Podemos contener un objeto List completo dentro de un estilo.
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

// Agregue algunos elementos de la lista que formateará nuestra lista.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Crear y aplicar otra lista basada en el estilo de lista.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


