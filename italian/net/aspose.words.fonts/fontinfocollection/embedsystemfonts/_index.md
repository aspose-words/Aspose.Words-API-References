---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words per .NET
description: FontInfoCollection EmbedSystemFonts proprietà. Specifica se incorporare o meno i caratteri di sistema nel documento. Il valore predefinito per questa proprietà èfalso in C#.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Specifica se incorporare o meno i caratteri di sistema nel documento. Il valore predefinito per questa proprietà è`falso`.

Questa opzione funziona solo quando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) l'opzione è impostata su`VERO`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Osservazioni

Impostazione di questa proprietà su`VERO`è utile se l'utente utilizza un sistema dell'Asia orientale e desidera creare un documento leggibile da altri che non dispongono di caratteri per quella lingua sul proprio sistema. Ad esempio, un utente su un sistema giapponese potrebbe scegliere di incorporare i caratteri in un documento in modo che il documento giapponese sia leggibile su tutti i sistemi.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

## Esempi

Mostra come salvare un documento con caratteri TrueType incorporati.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
