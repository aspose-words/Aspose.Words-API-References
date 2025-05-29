---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words per .NET
description: Ottimizza il tuo HTML con la funzione RemoveJavaScriptFromLinks di HtmlFixedSaveOptions. Migliora la sicurezza rimuovendo JavaScript dai link senza sforzo.
type: docs
weight: 140
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è`falso` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Osservazioni

Se questa opzione è abilitata, tutti i link contenenti JavaScript (ad esempio, i link con "javascript:" nell'attributo href) verranno sostituiti con "javascript:void(0)". Questo può aiutare a prevenire potenziali rischi per la sicurezza, come gli attacchi XSS.

## Esempi

Mostra come rimuovere JavaScript dai link.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Mostra come rimuovere JavaScript dai link per i documenti HTML corretti.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
