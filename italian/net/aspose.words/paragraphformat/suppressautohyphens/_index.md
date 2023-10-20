---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words per .NET
description: ParagraphFormat SuppressAutoHyphens proprietà. Specifica se il paragrafo corrente deve essere esentato da qualsiasi sillabazione che viene applicata nelle impostazioni del documento in C#.
type: docs
weight: 370
url: /it/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Specifica se il paragrafo corrente deve essere esentato da qualsiasi sillabazione che viene applicata nelle impostazioni del documento.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Esempi

Mostra come eliminare la sillabazione per un paragrafo.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Apre un documento contenente testo con una lingua corrispondente a quella del nostro dizionario.
// Quando salviamo questo documento in un formato di salvataggio della pagina fisso, il suo testo avrà una sillabazione.
Document doc = new Document(MyDir + "German text.docx");

// Possiamo impostare la proprietà "SuppressAutoHyphens" su "true" per disabilitare la sillabazione
// per un paragrafo specifico mantenendolo abilitato per il resto del documento.
// Il valore predefinito per questa proprietà è "false",
// il che significa che ogni paragrafo per impostazione predefinita utilizza la sillabazione, se disponibile.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
