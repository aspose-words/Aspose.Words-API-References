---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words para .NET
description: Navegue sin esfuerzo por su documento con el método MoveToParagraph de DocumentBuilder, que permite un movimiento rápido del cursor a cualquier párrafo de su sección.
type: docs
weight: 600
url: /es/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Mueve el cursor a un párrafo en la sección actual.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| paragraphIndex | Int32 | El índice del párrafo al que desea desplazarse. |
| characterIndex | Int32 | Índice del carácter dentro del párrafo. Un valor negativo permite especificar una posición desde el final del párrafo. Use -1 para ir al final del párrafo. |

## Observaciones

La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si movió el cursor al encabezado principal de la primera sección, entonces*paragraphIndex* especifica el índice del párrafo dentro de ese header de esa sección.

Cuando*paragraphIndex* es mayor o igual a 0, especifica un índice desde el inicio de la sección, siendo 0 el primer párrafo. Cuando*paragraphIndex* es menor que 0, especifica un índice desde el final de la sección con -1 siendo el último párrafo.

## Ejemplos

Muestra cómo mover la posición del cursor de un constructor a un párrafo específico.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Crea un generador de documentos para editar el documento. El cursor del generador,
// que es el punto donde insertará nuevos nodos cuando llamemos a sus métodos de construcción de documentos,
// se encuentra actualmente al principio del documento.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Mover ese cursor a un párrafo diferente colocará ese cursor delante de ese párrafo.
builder.MoveToParagraph(2, 0);
//Cualquier contenido nuevo que agreguemos se insertará en ese punto.
builder.Writeln("This is a new third paragraph. ");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
