---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words per .NET
description: Scopri il metodo GetMathRenderer di OfficeMath per convertire senza sforzo le equazioni in immagini, migliorando i tuoi documenti con elementi visivi chiari e professionali.
type: docs
weight: 90
url: /it/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Crea e restituisce un oggetto che può essere utilizzato per trasformare questa equazione in un'immagine.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Valore di ritorno

L'oggetto renderer per questa equazione.

## Osservazioni

Questo metodo richiama semplicemente il[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) costruttore e passa questo oggetto come parametro.

## Esempi

Mostra come eseguire il rendering di un oggetto Office Math in un file immagine nel file system locale.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Crea un oggetto "ImageSaveOptions" da passare al metodo "Save" del renderer del nodo per modificare
// come esegue il rendering del nodo OfficeMath in un'immagine.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Imposta la proprietà "Scala" su 5 per rendere l'oggetto cinque volte più grande della sua dimensione originale.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Guarda anche

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../../aspose.words.math/)
* assemblea [Aspose.Words](../../../)
