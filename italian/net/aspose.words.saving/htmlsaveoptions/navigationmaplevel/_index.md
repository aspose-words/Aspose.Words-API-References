---
title: HtmlSaveOptions.NavigationMapLevel
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica il livello massimo di intestazioni inserite nella mappa di navigazione durante lesportazione nei formati EPUB MOBI o AZW3 . Il valore predefinito è3 .
type: docs
weight: 390
url: /it/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Specifica il livello massimo di intestazioni inserite nella mappa di navigazione durante l'esportazione nei formati EPUB, MOBI o AZW3 . Il valore predefinito è`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

### Osservazioni

La mappa di navigazione consente agli interpreti di fornire un modo semplice di navigare attraverso la struttura del documento. Di solito i punti di navigazione corrispondono ai titoli nel documento. Per popolare le intestazioni fino al livello **N** assegna questo valore a`NavigationMapLevel`.

Per impostazione predefinita, vengono popolati tre livelli di intestazioni: paragrafi di stili **Rubrica 1** , **Rubrica 2** e **Rubrica 3**. È possibile impostare questa proprietà su un valore da 1 a 9 per richiedere il livello massimo corrispondente. Impostandola su zero ridurrà la mappa di navigazione solo alla radice del documento o alle radici delle parti del documento.

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


