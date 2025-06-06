---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words per .NET
description: Scopri la proprietà ForceCopyStyles di ImportFormatOptions e controlla facilmente la copia degli stili in modalità KeepSourceFormatting. Il valore predefinito è "false" per risultati ottimali.
type: docs
weight: 30
url: /it/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Ottiene o imposta un valore booleano che indica di copiare gli stili in conflitto inKeepSourceFormatting mode. Il valore predefinito è`falso` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Osservazioni

Per impostazione predefinita, se uno stile corrispondente esiste già in un documento di destinazione, lo stile di origine formatting viene espanso negli attributi del nodo diretto e lo stile di questo nodo viene reimpostato su quello predefinito.

Quando questa opzione è impostata su`VERO`, lo stile di origine verrà copiato forzatamente nel documento di destinazione con un nome univoco e applicato al nodo importato.

Nota che in questo caso non è garantito che la formattazione del nodo importato nel documento di destinazione verrà preservata.

## Esempi

Mostra come copiare forzatamente gli stili sorgente con nomi univoci.

```csharp
// Entrambi i documenti contengono MyStyle1 e MyStyle2, MyStyle3 esiste solo in un documento sorgente.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
