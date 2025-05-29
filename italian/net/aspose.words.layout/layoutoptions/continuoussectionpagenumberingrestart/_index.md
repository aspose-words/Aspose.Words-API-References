---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words per .NET
description: Scopri la proprietà LayoutOptions ContinuousSectionPageNumberingRestart per un controllo impeccabile della numerazione delle pagine nelle sezioni continue. Ottimizza il layout del tuo documento oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Osservazioni

Il valore predefinito èAlways . Corrisponde al comportamento di MS Word 2019, che era l'ultima versione al momento in cui è stata introdotta l'opzione. La vecchia logica di numerazione delle pagine dimostrata da MS Word 2016 è disponibile tramite questa opzione. Per favore[`ContinuousSectionRestart`](../../continuoussectionrestart/) per la descrizione del comportamento.

## Esempi

Mostra come controllare la numerazione delle pagine in una sezione continua.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Per impostazione predefinita, il comportamento di Aspose.Words corrisponde a quello di Microsoft Word 2019.
// Se è necessario il vecchio comportamento di Aspose.Words, ovvero Microsoft Word 2016 ripetitivo, utilizzare 'ContinuousSectionRestart.FromNewPageOnly'.
// La numerazione delle pagine ricomincia solo se non c'è altro contenuto prima della sezione nella pagina in cui inizia la sezione,
// Per questo motivo la numerazione verrà reimpostata su 2 a partire dalla seconda pagina.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Guarda anche

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
