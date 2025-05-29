---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.TabStopCollection. Gestione fácilmente tabulaciones personalizadas para párrafos y estilos, mejorando el formato de sus documentos con precisión.
type: docs
weight: 7060
url: /es/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Una colección de[`TabStop`](../tabstop/) objetos que representan pestañas personalizadas para un párrafo o un estilo.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Obtiene el número de tabulaciones en la colección. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Obtiene una tabulación en el índice dado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Agrega o reemplaza una tabulación en la colección. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Agrega o reemplaza una tabulación en la colección. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Obtiene la primera tabulación a la derecha de la posición especificada. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Obtiene la primera tabulación a la izquierda de la posición especificada. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Elimina todas las posiciones de tabulación. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Determina si el especificado`TabStopCollection` es igual en valor a la corriente`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Sirve como una función hash para este tipo. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Obtiene el índice de una tabulación con la posición especificada en puntos. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Obtiene la posición (en puntos) de la tabulación en el índice especificado. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Elimina una tabulación en el índice especificado de la colección. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Elimina una tabulación en la posición especificada de la colección. |

## Observaciones

En documentos de Microsoft Word, una tabulación se puede definir en las propiedades de un estilo de párrafo o directamente en las propiedades de un párrafo. Un estilo puede basarse en otro estilo. Por lo tanto, el conjunto completo de tabulaciones para un objeto dado es una combinación de tabulaciones definidas directamente en este objeto y tabulaciones heredadas de los estilos principales.

En Aspose.Words, cuando obtienes un`TabStopCollection` para un párrafo o un estilo, contiene solo las tabulaciones personalizadas definidas directamente para este párrafo o estilo. La colección no incluye tabulaciones definidas en los estilos principales o tabulaciones predeterminadas.

## Ejemplos

Muestra cómo trabajar con la colección de tabulaciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 puntos equivalen a una "pulgada" en la regla de tabulación de Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Cada carácter de "tabulación" lleva el cursor del constructor a la ubicación de la siguiente tabulación.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Cada párrafo obtiene su propia colección de tabulaciones, que clona sus valores de la colección de tabulaciones del generador de documentos.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Una colección de tabulaciones puede indicarnos tabulaciones antes y después de ciertas posiciones.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

//Podemos borrar la colección de tabulaciones de un párrafo para volver al comportamiento de tabulación predeterminado.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Ver también

* class [InternableComplexAttr](../internablecomplexattr/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
