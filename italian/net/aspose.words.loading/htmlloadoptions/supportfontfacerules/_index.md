---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words per .NET
description: Scopri il supporto di HtmlLoadOptions per FontFaceRules, controlla il caricamento dei font con facilità. Migliora il tuo web design abilitando font personalizzati per un look raffinato.
type: docs
weight: 60
url: /it/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Ottiene o imposta un valore che indica se supportare le regole @font-face e se caricare i font dichiarati. Il valore predefinito è `falso` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Osservazioni

Se questa opzione è abilitata, i font dichiarati nelle regole @font-face vengono caricati e incorporati nelle definizioni dei font del documento risultante (vedere[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Questo rende i font caricati disponibili per il rendering, ma non abilita automaticamente l'incorporamento dei font al momento del salvataggio. Per salvare il documento con i font caricati, il[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) proprietà del[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) La raccolta dovrebbe essere impostata su`VERO` .

I formati di font supportati sono TTF, EOT e WOFF.

Le regole @font-face non sono supportate durante il caricamento di immagini SVG.

## Esempi

Mostra come caricare le regole "@font-face" dichiarate.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
