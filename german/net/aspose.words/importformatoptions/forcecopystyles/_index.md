---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words für .NET
description: ImportFormatOptions ForceCopyStyles eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt ob widersprüchliche Stile kopiert werden sollenKeepSourceFormatting mode. Der Standardwert istFALSCH  in C#.
type: docs
weight: 30
url: /de/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob widersprüchliche Stile kopiert werden sollenKeepSourceFormatting mode. Der Standardwert ist`FALSCH` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Bemerkungen

Wenn in einem Zieldokument bereits ein passender Stil vorhanden ist, wird der Quellstil formatting standardmäßig in direkte Knotenattribute erweitert und der Stil dieses Knotens auf einen Standardwert zurückgesetzt.

Wenn diese Option auf eingestellt ist`WAHR`, wird der Quellstil zwangsweise in das Zieldokument mit eindeutigem Namen kopiert und auf den importierten Knoten angewendet.

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
