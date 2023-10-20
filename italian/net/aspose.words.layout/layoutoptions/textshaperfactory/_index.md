---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words per .NET
description: LayoutOptions TextShaperFactory proprietà. Ottiene o impostaITextShaperFactory implementazione utilizzata per le funzionalità di rendering di tipografia avanzata in C#.
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

// Aspose.Words può utilizzare oggetti modellatori di testo forniti esternamente,
// che rappresentano i caratteri e calcolano le informazioni sulla modellazione del testo.
// Una factory di modellazione del testo è necessaria per i documenti che utilizzano più font.
// Quando il modellatore di testo è impostato in fabbrica, il layout utilizza le funzionalità OpenType.
// Una proprietà Instance restituisce un oggetto statico BasicTextShaperCache che racchiude HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Attualmente, la modellazione del testo viene eseguita durante l'esportazione nei formati PDF o XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Guarda anche

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
