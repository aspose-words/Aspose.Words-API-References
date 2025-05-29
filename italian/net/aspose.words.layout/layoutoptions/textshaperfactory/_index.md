---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextShaperFactory di LayoutOptions per una tipografia avanzata. Migliora il tuo rendering con implementazioni personalizzabili di ITextShaperFactory.
type: docs
weight: 100
url: /it/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Ottiene o imposta[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) implementazione utilizzata per le funzionalità di rendering di tipografia avanzata.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Esempi

Mostra come supportare le funzionalità OpenType utilizzando il motore di modellazione del testo HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words può utilizzare oggetti di formattazione del testo forniti esternamente,
// che rappresentano i font e calcolano le informazioni di modellazione del testo.
// Per i documenti che utilizzano più font è necessaria una fabbrica di formattazione del testo.
// Quando il formato di testo è impostato in fabbrica, il layout utilizza le funzionalità OpenType.
// Una proprietà Instance restituisce un oggetto BasicTextShaperCache statico che racchiude HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Attualmente, la modellazione del testo funziona solo quando si esporta nei formati PDF o XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Guarda anche

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
