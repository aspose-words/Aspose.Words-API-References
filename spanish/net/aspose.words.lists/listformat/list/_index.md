---
title: ListFormat.List
second_title: Referencia de API de Aspose.Words para .NET
description: ListFormat propiedad. Obtiene o establece la lista a la que pertenece este párrafo.
type: docs
weight: 20
url: /es/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Obtiene o establece la lista a la que pertenece este párrafo.

```csharp
public List List { get; set; }
```

### Observaciones

La lista que se está asignando a esta propiedad debe pertenecer al documento actual.

La lista que se asigna a esta propiedad no debe ser una definición de estilo de lista.

Establecer esta propiedad en nulo elimina las viñetas y la numeración del párrafo y establece el número de nivel de lista en cero. Establecer esta propiedad en nulo es equivalente a llamar[`RemoveNumbers`](../removenumbers/).

### Ejemplos

Muestra cómo anidar una lista dentro de otra lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Crear una lista de esquemas para los encabezados.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Crea una lista numerada.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Cada párrafo que comprende una lista tendrá esta bandera.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Crear una lista con viñetas.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Volver a la lista numerada.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Volver a la lista de esquemas.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

Muestra cómo trabajar con niveles de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación hay dos tipos de listas que podemos crear usando un generador de documentos.
// 1 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para comenzar una sublista independiente en el elemento de la lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
// Los niveles de lista más profundos usan letras y números romanos en minúsculas. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista usarán diferentes símbolos, como "■" y "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Podemos deshabilitar el formato de la lista para no formatear los párrafos posteriores como listas al deshabilitar el indicador "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ver también

* class [List](../../list/)
* class [ListFormat](../)
* espacio de nombres [Aspose.Words.Lists](../../listformat/)
* asamblea [Aspose.Words](../../../)


