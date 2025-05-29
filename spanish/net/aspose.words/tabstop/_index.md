---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.TabStop, su solución para tabulaciones personalizadas en el formato de documentos. ¡Mejore sus documentos con precisión y facilidad!
type: docs
weight: 7050
url: /es/net/aspose.words/tabstop/
---
## TabStop class

Representa una única tabulación personalizada.`TabStop` El objeto es un miembro de the [`TabStopCollection`](../tabstopcollection/) colección.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public sealed class TabStop
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Inicializa una nueva instancia de esta clase. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Obtiene o establece la alineación del texto en esta tabulación. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Devuelve`verdadero` Si esta tabulación borra cualquier tabulación existente en esta posición. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Obtiene o establece el tipo de línea guía que se muestra debajo del carácter de tabulación. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Obtiene la posición de la tabulación en puntos. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Compara con el especificado`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Calcula el código hash para este objeto. |

## Observaciones

Normalmente, una tabulación especifica una posición donde existe. Sin embargo, dado que las tabulaciones pueden heredarse de los estilos principales, podría ser necesario que el objeto secundario defina explícitamente que no hay tabulaciones en una posición dada. Para borrar una tabulación heredada en una posición dada, cree un`TabStop` objeto y conjunto [`Alignment`](./alignment/) aClear.

Para más información véase[`TabStopCollection`](../tabstopcollection/).

## Ejemplos

Muestra cómo modificar la posición de la tabulación derecha en los párrafos relacionados con la tabla de contenidos.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterar a través de todos los párrafos con estilos basados en resultados de TOC; este es cualquier estilo entre TOC y TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Obtenga la primera tabulación utilizada en este párrafo, ésta debe ser la tabulación utilizada para alinear los números de página.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Reemplace la primera tabulación predeterminada con una tabulación personalizada.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
