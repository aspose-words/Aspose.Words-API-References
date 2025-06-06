---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words para .NET
description: Acceda al último párrafo de su historia sin esfuerzo con la propiedad Story LastParagraph, mejorando su experiencia de edición y gestión narrativa.
type: docs
weight: 20
url: /es/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Obtiene el último párrafo de la historia.

```csharp
public Paragraph LastParagraph { get; }
```

## Ejemplos

Muestra cómo mover la posición del cursor de un DocumentBuilder a un nodo específico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// El generador de documentos tiene un cursor, que actúa como parte del documento.
// donde el constructor agrega nuevos nodos cuando usamos sus métodos de construcción de documentos.
// Este cursor funciona de la misma manera que el cursor parpadeante de Microsoft Word,
// y también siempre termina inmediatamente después de cualquier nodo que el constructor acaba de insertar.
// Para agregar contenido a una parte diferente del documento,
//podemos mover el cursor a un nodo diferente con el método "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
//El cursor ahora está delante del nodo al que lo movimos.
//Agregar una segunda ejecución la insertará delante de la primera ejecución.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Mueva el cursor al final del documento para continuar agregando texto al final como antes.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Ver también

* class [Paragraph](../../paragraph/)
* class [Story](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
