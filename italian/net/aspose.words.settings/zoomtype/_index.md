---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Settings.ZoomType per personalizzare le dimensioni di visualizzazione dei documenti in Microsoft Word per una visualizzazione e una produttività ottimali.
type: docs
weight: 6810
url: /it/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Valori possibili per la dimensione del documento visualizzato sullo schermo in Microsoft Word.

```csharp
public enum ZoomType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Custom | `0` | La percentuale di zoom è impostata esplicitamente. Non viene ricalcolata automaticamente quando le dimensioni del controllo cambiano. |
| None | `0` | Indica di utilizzare la percentuale di zoom esplicita. ComeCustom . |
| FullPage | `1` | La percentuale di zoom viene ricalcolata automaticamente per adattarla a un'intera pagina. |
| PageWidth | `2` | La percentuale di zoom viene ricalcolata automaticamente per adattarsi alla larghezza della pagina. |
| TextFit | `3` | La percentuale di zoom viene ricalcolata automaticamente per adattare il testo. |

## Esempi

Mostra come impostare un fattore di zoom personalizzato che le vecchie versioni di Microsoft Word applicheranno a un documento al momento del caricamento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### Guarda anche

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
