---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: Spara dokument enkelt med IDocumentProcessorPlugin-metoden Spara, vilket säkerställer optimal utskrift med anpassningsbara sparalternativ för dina behov.
type: docs
weight: 30
url: /sv/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Spara dokumentet som laddades av[`Load`](../load/) metoden till utdataströmmen med hjälp av de angivna sparalternativen.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |

## Anmärkningar

Om det angivna utdataformatet är bild sparas endast den första sidans bild i utdataströmmen. Om det angivna sparformatet inte stöds direkt av plugin-programmet (kräver inläsning till[`Document`](../../document/)), -metoden kastar ett undantag.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
