---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words per .NET
description: Ottimizza il caricamento dei documenti con LoadOptions MswVersion. Garantisci la compatibilità con specifiche versioni di MS Word, impostando come impostazione predefinita Word 2019 per un'integrazione perfetta.
type: docs
weight: 100
url: /it/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito èWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Osservazioni

Diverse versioni di Word potrebbero gestire alcuni aspetti del contenuto e della formattazione del documento in modo leggermente diverso durante il processo di caricamento, il che potrebbe comportare piccole differenze nel Document Object Model.

## Esempi

Mostra come emulare la procedura di caricamento di una versione specifica di Microsoft Word durante il caricamento del documento.

```csharp
// Per impostazione predefinita, Aspose.Words carica i documenti in base alle specifiche di Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// In questo documento manca lo stile di formattazione del paragrafo predefinito.
// Questo stile predefinito verrà rigenerato quando caricheremo il documento con Microsoft Word o Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// La spaziatura delle linee dello stile avrà questo valore quando caricato dalle specifiche di Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Guarda anche

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
