---
title: Enum ContinuousSectionRestart
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.ContinuousSectionRestart enum. Rappresenta comportamenti diversi durante il calcolo dei numeri di pagina in una sezione continua che riavvia la numerazione delle pagine.
type: docs
weight: 3300
url: /it/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Rappresenta comportamenti diversi durante il calcolo dei numeri di pagina in una sezione continua che riavvia la numerazione delle pagine.

```csharp
public enum ContinuousSectionRestart
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Always | `0` | La numerazione delle pagine ricomincia sempre indipendentemente dal flusso dei contenuti. |
| FromNewPageOnly | `1` | La numerazione delle pagine ricomincia solo se non c'è altro contenuto prima della sezione nella pagina in cui inizia la sezione. |

### Esempi

Mostra come controllare la numerazione delle pagine in una sezione continua.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Per impostazione predefinita, il comportamento di Aspose.Words corrisponde a Microsoft Word 2019.
// Se è necessario il vecchio comportamento Aspose.Words, Microsoft Word 2016 ripetitivo, utilizzare "ContinuousSectionRestart.FromNewPageOnly".
// La numerazione delle pagine ricomincia solo se non c'è altro contenuto prima della sezione nella pagina in cui inizia la sezione,
// per questo motivo la numerazione verrà ripristinata a 2 dalla seconda pagina.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)


