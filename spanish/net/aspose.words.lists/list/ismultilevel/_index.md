---
title: List.IsMultiLevel
second_title: Referencia de API de Aspose.Words para .NET
description: List propiedad. Devuelve verdadero cuando la lista contiene 9 niveles falso cuando 1 nivel.
type: docs
weight: 40
url: /es/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

Devuelve verdadero cuando la lista contiene 9 niveles; falso cuando 1 nivel.

```csharp
public bool IsMultiLevel { get; }
```

### Observaciones

Las listas que crea con Aspose.Words son siempre listas de varios niveles y contienen 9 niveles.

Microsoft Word 2003 y posteriores siempre crean listas de varios niveles con 9 niveles. Pero en algunos documentos, creados con versiones anteriores de Microsoft Word, puede encontrar listas que tienen solo 1 nivel.

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

* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../list/)
* asamblea [Aspose.Words](../../../)


