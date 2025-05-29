---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SupportVml di HtmlLoadOptions migliora la tua esperienza web abilitando il supporto delle immagini VML per una migliore qualità grafica.
type: docs
weight: 70
url: /it/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Ottiene o imposta un valore che indica se supportare le immagini VML.

```csharp
public bool SupportVml { get; set; }
```

## Esempi

Mostra come supportare i commenti condizionali durante il caricamento di un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Se il valore è true, prendiamo in considerazione il codice VML durante l'analisi del documento caricato.
loadOptions.SupportVml = supportVml;

// Questo documento contiene un'immagine JPEG tra i tag "<!--[if gte vml 1]>",
// e un'immagine PNG diversa all'interno dei tag "<![if !vml]>".
// Se impostiamo il flag "SupportVml" su "true", Aspose.Words caricherà il JPEG.
// Se impostiamo questo flag su "false", Aspose.Words caricherà solo il PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
