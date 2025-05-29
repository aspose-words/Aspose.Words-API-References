---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ShapeBase ZOrder migliora il tuo design controllando l'ordine di visualizzazione delle forme sovrapposte, per un layout più chiaro e organizzato.
type: docs
weight: 650
url: /it/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Determina l'ordine di visualizzazione delle forme sovrapposte.

```csharp
public int ZOrder { get; set; }
```

## Osservazioni

Ha effetto solo sulle forme di livello superiore.

Il valore predefinito è 0.

Il numero rappresenta la precedenza di sovrapposizione. Una forma con un numero più alto verrà visualizzata come se si sovrapponesse (ovvero "davanti") a una forma con un numero più basso.

L'ordine delle forme sovrapposte è indipendente per le forme nell'intestazione e nel testo main del documento.

L'ordine di visualizzazione delle forme figlio in un gruppo di forme è determinato dal loro ordine all'interno del gruppo di forme.

## Esempi

Mostra come manipolare l'ordine delle forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci tre rettangoli di colore diverso che si sovrappongono parzialmente.
// Quando inseriamo una forma che si sovrappone a un'altra forma, Aspose.Words posiziona la forma più nuova sopra quella vecchia.
// Il rettangolo verde chiaro si sovrapporrà al rettangolo azzurro e lo oscurerà parzialmente,
// e il rettangolo azzurro nasconderà il rettangolo arancione.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// La proprietà "ZOrder" di una forma determina la sua priorità di accatastamento tra le altre forme sovrapposte.
// Se due forme sovrapposte hanno valori "ZOrder" diversi,
 // Microsoft Word posizionerà la forma con il valore più alto sopra quella con il valore più basso.
// Imposta i valori "ZOrder" delle nostre forme per posizionare il primo rettangolo arancione sopra il secondo azzurro
// e il secondo rettangolo azzurro chiaro sopra il terzo rettangolo verde chiaro.
// Questo invertirà il loro ordine di impilamento originale.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
