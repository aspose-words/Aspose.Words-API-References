---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words per .NET
description: LoadOptions MswVersion proprietà. Permette di specificare che il processo di caricamento del documento deve corrispondere a una specifica versione di MS Word. Il valore predefinito èWord2019 in C#.
type: docs
weight: 100
url: /it/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Permette di specificare che il processo di caricamento del documento deve corrispondere a una specifica versione di MS Word. Il valore predefinito èWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Osservazioni

Versioni diverse di Word potrebbero gestire alcuni aspetti del contenuto del documento e della formattazione in modo leggermente diverso durante il processo di caricamento, il che potrebbe comportare piccole differenze nel Document Object Model.

## Esempi

Mostra come emulare la procedura di caricamento di una specifica versione di Microsoft Word durante il caricamento del documento.

```csharp
// Per impostazione predefinita, Aspose.Words carica i documenti secondo le specifiche di Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// In questo documento manca lo stile di formattazione del paragrafo predefinito.
// Questo stile predefinito verrà rigenerato quando carichiamo il documento con Microsoft Word o Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// L'interlinea dello stile avrà questo valore quando viene caricata dalle specifiche di Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Guarda anche

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
