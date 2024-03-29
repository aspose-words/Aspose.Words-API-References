---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words per .NET
description: HtmlFixedSaveOptions OptimizeOutput proprietà. Il flag indica se è necessario ottimizzare loutput. Se questo flag è impostato le tele nidificate ridondanti e le tele vuote vengono rimosse vengono concatenati anche i glifi vicini con la stessa formattazione. Nota la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata suVERO . Limpostazione predefinita èVERO  in C#.
type: docs
weight: 100
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, vengono concatenati anche i glifi vicini con la stessa formattazione. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su`VERO` . L'impostazione predefinita è`VERO` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Esempi

Mostra come semplificare un documento quando lo si salva in HTML rimuovendo vari oggetti ridondanti.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// La dimensione della versione ottimizzata del documento è quasi un terzo della dimensione del documento non ottimizzato.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
