---
title: ListFormat.RemoveNumbers
linktitle: RemoveNumbers
articleTitle: RemoveNumbers
second_title: Aspose.Words para .NET
description: Elimine sin esfuerzo números o viñetas de sus párrafos con el método ListFormat RemoveNumbers, restableciendo el nivel de su lista a cero para un formato limpio.
type: docs
weight: 90
url: /es/net/aspose.words.lists/listformat/removenumbers/
---
## ListFormat.RemoveNumbers method

Elimina números o viñetas del párrafo actual y establece el nivel de lista en cero.

```csharp
public void RemoveNumbers()
```

## Observaciones

Llamar a este método es equivalente a configurar el[`List`](../list/) propiedad a`nulo`.

## Ejemplos

Muestra cómo eliminar el formato de lista de todos los párrafos del texto principal de una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);
Assert.AreEqual(3, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));

foreach (Paragraph paragraph in paras)
    paragraph.ListFormat.RemoveNumbers();

Assert.AreEqual(0, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));
```

Muestra cómo crear listas numeradas y con viñetas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
//A continuación se muestran dos tipos de listas que podemos crear con un generador de documentos.
// 1 - Una lista con viñetas:
//Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

//Fin de la lista con viñetas.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.ApplyNumberDefault();

Este párrafo es el primer elemento. El primer elemento de una lista numerada tendrá un "1." como símbolo.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Llama al método "ListIndent" para aumentar el nivel de lista actual,
// que iniciará una nueva lista autónoma, con una sangría más profunda, en el elemento actual del primer nivel de lista.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Estos son los primeros tres elementos de la lista del segundo nivel de lista, que mantendrá un recuento
// independiente del recuento del primer nivel de lista. Según el formato de lista actual,
// tendrán los símbolos "a.", "b." y "c."
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Llame al método "ListOutdent" para regresar al nivel de lista anterior.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

//Estos dos párrafos continuarán el recuento del primer nivel de lista.
// Estos elementos tendrán los símbolos "2." y "3."
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Si aumentamos el nivel de la lista a un nivel al que hemos agregado elementos previamente,
 //la lista anidada estará separada de la anterior y su numeración comenzará desde el principio.
// Estos elementos de lista tendrán los símbolos "a.", "b.", "c.", "d." y "e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Vuelve a anular la sangría del nivel de lista.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

//Fin de la lista numerada.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Ver también

* class [ListFormat](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
