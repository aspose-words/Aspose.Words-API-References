---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words per .NET
description: Migliora l'output dei tuoi documenti con la proprietà OptimizeOutput di FixedPageSaveOptions. Rimuovi le ridondanze e migliora la formattazione per visualizzazioni più chiare.
type: docs
weight: 50
url: /it/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su`VERO` . Il valore predefinito è`falso` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Esempi

Mostra come ottimizzare gli oggetti del documento durante il salvataggio in formato XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Crea un oggetto "XpsSaveOptions" da passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// Imposta la proprietà "OptimizeOutput" su "true" per adottare misure come la rimozione di canvas nidificati o vuoti
// e concatenando esecuzioni adiacenti con formattazione identica per ottimizzare il contenuto del documento di output.
// Ciò potrebbe influire sull'aspetto del documento.
// Impostare la proprietà "OptimizeOutput" su "false" per salvare il documento normalmente.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Guarda anche

* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
