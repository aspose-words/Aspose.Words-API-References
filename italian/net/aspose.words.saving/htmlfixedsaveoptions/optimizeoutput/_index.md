---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words per .NET
description: Ottimizza l'output HTML con la proprietà HtmlFixedSaveOptions. Migliora le prestazioni rimuovendo i canvas ridondanti e unendo glifi simili. Valore predefinito: true.
type: docs
weight: 110
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su`VERO` . Il valore predefinito è`VERO` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Esempi

Mostra come semplificare un documento salvandolo in formato HTML, rimuovendo vari oggetti ridondanti.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// La dimensione della versione ottimizzata del documento è quasi un terzo di quella del documento non ottimizzato.
Assert.AreEqual(optimizeOutput ? 60385 : 191000,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
