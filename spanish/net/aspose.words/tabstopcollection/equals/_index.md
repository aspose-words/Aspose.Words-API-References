---
title: TabStopCollection.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words para .NET
description: Descubra el método TabStopCollection Equals para comparar fácilmente TabStopCollections en busca de igualdad, mejorando así la eficiencia y precisión de su codificación.
type: docs
weight: 70
url: /es/net/aspose.words/tabstopcollection/equals/
---
## Equals(*[TabStopCollection](../)*) {#equals}

Determina si el especificado[`TabStopCollection`](../) es igual en valor a la corriente[`TabStopCollection`](../) .

```csharp
public bool Equals(TabStopCollection rhs)
```

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

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Determina si el objeto especificado es igual en valor al objeto actual.

```csharp
public override bool Equals(object obj)
```

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

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
