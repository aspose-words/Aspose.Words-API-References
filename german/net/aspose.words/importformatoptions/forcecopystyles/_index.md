---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ImportFormatOptions ForceCopyStyles“ und steuern Sie das Kopieren von Stilen im KeepSourceFormatting-Modus ganz einfach. Für optimale Ergebnisse ist der Standardwert „false“.
type: docs
weight: 30
url: /de/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob widersprüchliche Stile kopiert werden sollen inKeepSourceFormatting mode. Der Standardwert ist`FALSCH` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Bemerkungen

Wenn in einem Zieldokument bereits ein passender Stil vorhanden ist, wird standardmäßig der Quellstil formatting in direkte Knotenattribute erweitert und der Stil dieses Knotens auf einen Standard zurückgesetzt.

Wenn diese Option auf`WAHR`, der Quellstil wird zwangsweise mit einem eindeutigen Namen in das Zieldokument kopiert und auf den importierten Knoten angewendet.

Beachten Sie, dass in diesem Fall nicht garantiert werden kann, dass die Formatierung des importierten Knotens im Zieldokument erhalten bleibt.

## Beispiele

Zeigt, wie Quellstile mit eindeutigen Namen zwangsweise kopiert werden.

```csharp
// Beide Dokumente enthalten MyStyle1 und MyStyle2, MyStyle3 existiert nur in einem Quelldokument.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
