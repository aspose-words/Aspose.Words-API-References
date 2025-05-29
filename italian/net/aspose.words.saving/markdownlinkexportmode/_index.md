---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words per .NET
description: Scopri come l'enum Aspose.Words MarkdownLinkExportMode migliora l'esportazione dei link in Markdown, ottimizzando senza sforzo il processo di conversione dei documenti.
type: docs
weight: 6030
url: /it/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Specifica come i collegamenti vengono esportati in Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Rileva automaticamente la modalità di esportazione per ogni collegamento. |
| Inline | `1` | Esporta tutti i collegamenti come blocchi in linea. |
| Reference | `2` | Esporta tutti i collegamenti come blocchi di riferimento. |

## Esempi

Mostra come i collegamenti verranno scritti nel file .md.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// L'immagine verrà scritta come riferimento:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// L'immagine verrà scritta in linea:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
