---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words per .NET
description: Scopri la proprietà IdPrefix di HtmlFixedSaveOptions per personalizzare gli ID degli elementi nei tuoi documenti. Migliora l'organizzazione con prefissi personalizzati per un output migliore!
type: docs
weight: 100
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

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

Mostra come aggiungere un prefisso da anteporre a tutti gli ID degli elementi generati.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
