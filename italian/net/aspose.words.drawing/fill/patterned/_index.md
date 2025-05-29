---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words per .NET
description: Scopri il metodo Fill Patterned per applicare senza sforzo motivi unici ai tuoi progetti, migliorando la creatività e l'attrattiva visiva dei tuoi progetti.
type: docs
weight: 230
url: /it/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Imposta il riempimento specificato su un motivo.

```csharp
public void Patterned(PatternType patternType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

## Esempi

Mostra come impostare un pattern per una forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Esistono diversi modi per specificare il riempimento di un pattern.
// 1 - Applica il motivo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Applica il motivo con colori di primo piano e di sfondo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Guarda anche

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Imposta il riempimento specificato su un motivo.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Colore di riempimento in primo piano. |
| backColor | Color | Colore di riempimento dello sfondo. |

## Esempi

Mostra come impostare un pattern per una forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Esistono diversi modi per specificare il riempimento di un pattern.
// 1 - Applica il motivo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Applica il motivo con colori di primo piano e di sfondo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Guarda anche

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
