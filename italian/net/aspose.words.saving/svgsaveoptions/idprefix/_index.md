---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words per .NET
description: Scopri la proprietà IdPrefix di SvgSaveOptions, che personalizza gli ID degli elementi nel documento di output per una migliore organizzazione e chiarezza. Migliora i tuoi file SVG oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

Specifica un prefisso da aggiungere a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e non viene aggiunto alcun prefisso.

```csharp
public string IdPrefix { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Il valore non soddisfa i requisiti specificati sopra. |

## Osservazioni

Se il prefisso è specificato, può contenere solo lettere, cifre, caratteri di sottolineatura e trattini, e deve iniziare con una lettera.

## Esempi

Mostra come aggiungere un prefisso da anteporre a tutti gli ID degli elementi generati (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Guarda anche

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
