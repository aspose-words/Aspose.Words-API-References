---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words para .NET
description: Optimice su contenido con el método EnsureMinimum, garantizando que cada sección incluya un Cuerpo con un Párrafo para una mayor claridad y estructura.
type: docs
weight: 150
url: /es/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Asegura que la sección tenga[`Body`](../body/) con uno[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Ejemplos

Muestra cómo preparar un nuevo nodo de sección para su edición.

```csharp
Document doc = new Document();

// Un documento en blanco viene con una sección, que tiene un cuerpo, que a su vez tiene un párrafo.
//Podemos agregar contenidos a este documento añadiendo elementos como líneas de texto, formas o tablas a ese párrafo.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Si agregamos una nueva sección como esta, no tendrá cuerpo ni ningún otro nodo secundario.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Ejecute el método "EnsureMinimum" para agregar un cuerpo y un párrafo a esta sección para comenzar a editarla.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
