---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.ReflectionFormat per una formattazione avanzata della riflessione degli oggetti. Migliora il design dei tuoi documenti con un'integrazione perfetta!
type: docs
weight: 1570
url: /it/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Rappresenta la formattazione della riflessione per un oggetto.

```csharp
public class ReflectionFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Ottiene o imposta un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. Il valore predefinito è 0.0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Ottiene o imposta un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. Il valore predefinito è 0.0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Ottiene o imposta un valore double compreso tra 0,0 e 1,0 che rappresenta la dimensione del riflesso come percentuale dell'oggetto riflesso. Il valore predefinito è 0,0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Ottiene o imposta un valore double compreso tra 0,0 (opaco) e 1,0 (trasparente) che rappresenta il grado di trasparenza per l'effetto di riflessione. Il valore predefinito è 0,0. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Rimuove`ReflectionFormat` dall'oggetto padre. |

## Osservazioni

Utilizzare il[`Reflection`](../shapebase/reflection/) proprietà per accedere alle proprietà di riflessione di un oggetto. Non si creano istanze di`ReflectionFormat` classe direttamente.

## Esempi

Mostra come interagire con l'effetto forma riflesso.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
