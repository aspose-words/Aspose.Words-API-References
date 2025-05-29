---
title: TabStopCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a las tabulaciones con la propiedad Item de TabStopCollection. Recupere tabulaciones específicas por índice para una navegación eficiente en la interfaz de usuario.
type: docs
weight: 20
url: /es/net/aspose.words/tabstopcollection/item/
---
## TabStopCollection indexer (1 of 2)

Obtiene una tabulación en el índice dado.

```csharp
public TabStop this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección de tabulaciones. |

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

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## TabStopCollection indexer (2 of 2)

Obtiene una tabulación en la posición especificada.

```csharp
public TabStop this[double position] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| position | La posición (en puntos) de la tabulación. |

## Observaciones

Devuelve`nulo` si no se encuentra ninguna tabulación en la posición especificada.

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

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
