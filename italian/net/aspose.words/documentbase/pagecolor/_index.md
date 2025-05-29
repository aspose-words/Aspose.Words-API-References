---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageColor di DocumentBase per personalizzare facilmente il colore di pagina del tuo documento. Semplifica la progettazione con questa funzionalità intuitiva!
type: docs
weight: 70
url: /it/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione semplificata di[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Osservazioni

Questa proprietà fornisce un modo semplice per specificare un colore di pagina pieno per il documento. L'impostazione di questa proprietà crea e imposta un colore appropriato[`BackgroundShape`](../backgroundshape/).

Se il colore della pagina non è impostato (ad esempio non c'è una forma di sfondo nel documento) restituisce Empty.

## Esempi

Mostra come impostare il colore di sfondo per tutte le pagine di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Guarda anche

* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
