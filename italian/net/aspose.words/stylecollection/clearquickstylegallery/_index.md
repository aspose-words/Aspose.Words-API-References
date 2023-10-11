---
title: StyleCollection.ClearQuickStyleGallery
second_title: Aspose.Words per .NET API Reference
description: StyleCollection metodo. Rimuove tutti gli stili dal pannello Galleria stili veloci.
type: docs
weight: 80
url: /it/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Rimuove tutti gli stili dal pannello Galleria stili veloci.

```csharp
public void ClearQuickStyleGallery()
```

### Esempi

Mostra come rimuovere gli stili dal pannello Galleria di stili.

```csharp
Document doc = new Document();
// Tieni presente che per il momento la rimozione degli stili funziona solo con il formato DOCX.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Guarda anche

* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../stylecollection/)
* assemblea [Aspose.Words](../../../)


