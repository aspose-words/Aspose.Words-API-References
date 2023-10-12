---
title: DocumentBuilder.MoveToParagraph
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Mueve el cursor a un párrafo en la sección actual.
type: docs
weight: 570
url: /es/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Mueve el cursor a un párrafo en la sección actual.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| paragraphIndex | Int32 | El índice del párrafo al que pasar. |
| characterIndex | Int32 | El índice del carácter dentro del párrafo. Un valor negativo le permite especificar una posición desde el final del párrafo. Utilice -1 para desplazarse al final de el párrafo. |

### Observaciones

La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si movió el cursor al encabezado principal de la primera sección, entonces*paragraphIndex*especificó el índice del párrafo dentro de ese header de esa sección.

Cuando*paragraphIndex* es mayor o igual a 0, especifica un índice desde el comienzo de la sección siendo 0 el primer párrafo. Cuando*paragraphIndex* es menor que 0, , especificó un índice desde el final de la sección, siendo -1 el último párrafo.

### Ejemplos

Muestra cómo mover la posición del cursor de un constructor a un párrafo específico.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Crear generador de documentos para editar el documento. El cursor del constructor,
// que es el punto donde insertará nuevos nodos cuando llamemos a sus métodos de construcción de documentos,
// se encuentra actualmente al comienzo del documento.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Mover ese cursor a un párrafo diferente colocará ese cursor delante de ese párrafo.
builder.MoveToParagraph(2, 0);
// Cualquier contenido nuevo que agreguemos se insertará en ese punto.
builder.Writeln("This is a new third paragraph. ");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


