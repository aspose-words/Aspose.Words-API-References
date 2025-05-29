---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShowHiddenText di LayoutOptions e controlla facilmente la visualizzazione del testo nascosto nei tuoi documenti. Ottimizza la visibilità dei tuoi contenuti oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Ottiene o imposta l'indicazione se il testo nascosto nel documento viene renderizzato. Il valore predefinito è`falso` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Osservazioni

Questa proprietà ha effetto su tutti i contenuti nascosti, non solo sul testo.

## Esempi

Mostra come nascondere il testo in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserisce il testo nascosto, quindi specifica se desideriamo ometterlo dal documento renderizzato.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
