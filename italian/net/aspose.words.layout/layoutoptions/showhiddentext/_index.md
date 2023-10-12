---
title: LayoutOptions.ShowHiddenText
second_title: Aspose.Words per .NET API Reference
description: LayoutOptions proprietà. Ottiene o imposta lindicazione se viene eseguito il rendering del testo nascosto nel documento. Limpostazione predefinita èfalso .
type: docs
weight: 80
url: /it/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Ottiene o imposta l'indicazione se viene eseguito il rendering del testo nascosto nel documento. L'impostazione predefinita è`falso` .

```csharp
public bool ShowHiddenText { get; set; }
```

### Osservazioni

Questa proprietà influisce su tutto il contenuto nascosto, non solo sul testo.

### Esempi

Mostra come nascondere il testo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserisci il testo nascosto, quindi specifica se desideriamo ometterlo da un documento renderizzato.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../layoutoptions/)
* assemblea [Aspose.Words](../../../)


