---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Aspose.Words per .NET API Reference
description: LayoutOptions proprietà. Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine.
type: docs
weight: 40
url: /it/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### Osservazioni

Il valore predefinito èAlways . Corrisponde al comportamento di MS Word 2019, che era l'ultima versione al momento dell'introduzione dell'opzione. La logica di numerazione delle pagine precedente dimostrata da MS Word 2016 è disponibile tramite questa opzione. Per favore[`ContinuousSectionRestart`](../../continuoussectionrestart/) per la descrizione del comportamento.

### Esempi

Mostra come controllare la numerazione delle pagine in una sezione continua.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Per impostazione predefinita, il comportamento di Aspose.Words corrisponde a Microsoft Word 2019.
// Se hai bisogno del vecchio comportamento di Aspose.Words, ripetitivo di Microsoft Word 2016, usa 'ContinuousSectionRestart.FromNewPageOnly'.
// La numerazione delle pagine riprende solo se non sono presenti altri contenuti prima della sezione della pagina in cui inizia la sezione,
// per questo motivo la numerazione verrà ripristinata a 2 dalla seconda pagina.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Guarda anche

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../layoutoptions/)
* assemblea [Aspose.Words](../../../)


