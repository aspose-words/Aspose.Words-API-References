---
title: TabStopCollection.GetHashCode
second_title: Referencia de API de Aspose.Words para .NET
description: TabStopCollection método. Sirve como función hash para este tipo.
type: docs
weight: 80
url: /es/net/aspose.words/tabstopcollection/gethashcode/
---
## TabStopCollection.GetHashCode method

Sirve como función hash para este tipo.

```csharp
public override int GetHashCode()
```

### Ejemplos

Muestra cómo trabajar con la colección de tabulaciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 puntos es una "pulgada" en la regla de tabulación de Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Cada carácter de "tabulador" lleva el cursor del constructor a la ubicación de la siguiente tabulación.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Cada párrafo obtiene su colección de tabulaciones, que clona sus valores de la colección de tabulaciones del generador de documentos.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Una colección de tabulaciones puede señalarnos TabStops antes y después de ciertas posiciones.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Podemos borrar la colección de tabulaciones de un párrafo para volver al comportamiento de tabulación predeterminado.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Ver también

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../tabstopcollection/)
* asamblea [Aspose.Words](../../../)


