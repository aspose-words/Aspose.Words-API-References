---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words per .NET
description: ChmLoadOptions OriginalFileName proprietà. Il nome del file CHM. Il valore predefinito ènullo  in C#.
type: docs
weight: 20
url: /it/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

Il nome del file CHM. Il valore predefinito è`nullo` .

```csharp
public string OriginalFileName { get; set; }
```

## Osservazioni

I documenti CHM possono contenere collegamenti che fanno riferimento allo stesso documento tramite il nome del file. Aspose.Words supporta tali links e normalmente utilizza[`OriginalFileName`](../../../aspose.words/document/originalfilename/) per verificare se il file a cui fa riferimento un link è il file che viene caricato. Se un documento viene caricato da uno stream, il nome del file originale deve essere specificato esplicitamente tramite questa proprietà, poiché non può essere determinato automaticamente.

Se un documento CHM viene caricato da un file e viene specificato un valore non nullo per questa proprietà, il valore avrà priorità rispetto al nome effettivo del file archiviato in[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## Esempi

Mostra come risolvere URL come "ms-its:myfile.chm::/index.htm".

```csharp
// Il nostro documento contiene URL come "ms-its:amhelp.chm::....htm", ma ha un nome diverso,
// quindi i collegamenti ai file non funzionano dopo averlo salvato in HTML.
// Dobbiamo definire il nome file originale in 'ChmLoadOptions' per evitare questo comportamento.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Guarda anche

* class [ChmLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
