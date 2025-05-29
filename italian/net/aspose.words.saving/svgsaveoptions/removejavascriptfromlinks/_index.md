---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words per .NET
description: Ottimizza i file SVG con SvgSaveOptions e rimuovi facilmente JavaScript dai link per un codice più pulito. Migliora prestazioni e sicurezza con questa semplice impostazione!
type: docs
weight: 60
url: /it/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è`falso` . Se questa opzione è abilitata, tutti i link contenenti JavaScript verranno sostituiti con "javascript:void(0)".

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Esempi

Mostra come rimuovere JavaScript dai link (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Guarda anche

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
