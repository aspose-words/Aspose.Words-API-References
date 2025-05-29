---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words per .NET
description: Controlla la sillabazione nel tuo documento con la proprietà ParagraphFormat SuppressAutoHyphens, assicurando una formattazione dei paragrafi chiara e professionale.
type: docs
weight: 380
url: /it/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Specifica se il paragrafo corrente deve essere esentato da qualsiasi sillabazione applicata nelle impostazioni del documento.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Esempi

Mostra come eliminare la sillabazione in un paragrafo.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Apre un documento contenente testo con impostazioni locali corrispondenti a quelle del nostro dizionario.
// Quando salviamo questo documento in un formato di salvataggio a pagina fissa, il testo sarà suddiviso in sillabe.
Document doc = new Document(MyDir + "German text.docx");

// Possiamo impostare la proprietà "SuppressAutoHyphens" su "true" per disabilitare la sillabazione
// per un paragrafo specifico mantenendolo abilitato per il resto del documento.
// Il valore predefinito per questa proprietà è "false",
// il che significa che per impostazione predefinita ogni paragrafo utilizza la sillabazione, se disponibile.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
