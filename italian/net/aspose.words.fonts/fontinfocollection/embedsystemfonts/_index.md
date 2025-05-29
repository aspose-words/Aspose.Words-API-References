---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FontInfoCollection EmbedSystemFonts migliora i tuoi documenti incorporando i font di sistema. Scopri il suo valore predefinito e i suoi vantaggi!
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Specifica se incorporare o meno i font di sistema nel documento. Il valore predefinito per questa proprietà è`falso`.

Questa opzione funziona solo quando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) l'opzione è impostata su`VERO`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Osservazioni

Impostando questa proprietà su`VERO` È utile se l'utente utilizza un sistema dell'Asia orientale e desidera creare un documento leggibile da altri che non dispongono di font per quella lingua sul proprio sistema. Ad esempio, un utente di un sistema giapponese potrebbe scegliere di incorporare i font in un documento in modo che il documento giapponese sia leggibile su tutti i sistemi.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

## Esempi

Mostra come salvare un documento con i font TrueType incorporati.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
