---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words per .NET
description: Scopri il metodo AddPrinterFont di PclSaveOptions per caricare e gestire in modo efficiente i font per stampante dei produttori, per ottenere prestazioni di stampa migliori.
type: docs
weight: 50
url: /it/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Aggiunge informazioni sul font caricato sulla stampante dal produttore.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFullName | String | Nome completo del font (ad esempio "Times New Roman Bold Italic"). |
| fontPclName | String | Nome del font utilizzato nel documento Pcl. |

## Osservazioni

Ci sono 52 font che devono essere integrati in qualsiasi stampante secondo le specifiche Pcl. Tuttavia i produttori possono aggiungere altri font ai loro dispositivi.

## Esempi

Mostra come fare in modo che una stampante sostituisca tutte le istanze di un font specifico con un font diverso.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Quando si stampa questo documento, la stampante utilizzerà il font "Courier New"
// per accedere ai punti in cui il nostro documento utilizzava il font "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Guarda anche

* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
