---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words per .NET
description: Esplora l'enumerazione Aspose.Words.Layout.ContinuousSectionRestart per opzioni di numerazione delle pagine flessibili in sezioni continue. Migliora il layout del documento senza sforzo!
type: docs
weight: 3750
url: /it/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Rappresenta diversi comportamenti durante il calcolo dei numeri di pagina in una sezione continua che riavvia la numerazione delle pagine.

```csharp
public enum ContinuousSectionRestart
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Always | `0` | La numerazione delle pagine ricomincia sempre, indipendentemente dal flusso dei contenuti. |
| FromNewPageOnly | `1` | La numerazione delle pagine ricomincia solo se non c'è altro contenuto prima della sezione nella pagina in cui inizia la sezione. |

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

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
