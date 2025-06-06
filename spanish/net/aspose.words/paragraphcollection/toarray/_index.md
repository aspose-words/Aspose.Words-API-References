---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words para .NET
description: Convierta sin esfuerzo su ParagraphCollection en una matriz con el método ToArray, agilizando la gestión de datos y mejorando el procesamiento de sus documentos.
type: docs
weight: 20
url: /es/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Copia todos los párrafos de la colección a una nueva matriz de párrafos.

```csharp
public Paragraph[] ToArray()
```

### Valor_devuelto

Una serie de párrafos.

## Ejemplos

Muestra cómo crear una matriz a partir de una NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Muestra cómo utilizar la "eliminación activa" para eliminar un nodo durante la enumeración.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

//Eliminar un nodo de la colección en medio de una enumeración.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Ver también

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
