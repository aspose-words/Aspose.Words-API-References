---
title: ParagraphFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: Restablezca el formato de sus párrafos sin esfuerzo con el método ClearFormatting, garantizando una apariencia pulida y profesional para sus documentos.
type: docs
weight: 430
url: /es/net/aspose.words/paragraphformat/clearformatting/
---
## ParagraphFormat.ClearFormatting method

Restablece el formato de párrafo predeterminado.

```csharp
public void ClearFormatting()
```

## Observaciones

El formato de párrafo predeterminado es el estilo Normal, alineado a la izquierda, sin sangría, sin espaciado, sin bordes y sin sombreado.

## Ejemplos

Muestra cómo anidar una lista dentro de otra lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Crear una lista de esquema para los encabezados.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

//Crea una lista numerada.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

//Cada párrafo que compone una lista tendrá esta bandera.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Crea una lista con viñetas.
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

// Volver a la lista de esquema.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
