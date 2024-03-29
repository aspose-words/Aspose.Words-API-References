---
title: SaveOptions.UpdateSdtContent
second_title: Aspose.Words per .NET API Reference
description: SaveOptions proprietà. Ottiene o imposta il valore che determina se il contenuto diStructuredDocumentTag viene aggiornato prima del salvataggio.
type: docs
weight: 200
url: /it/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) viene aggiornato prima del salvataggio.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Osservazioni

Il valore predefinito è`VERO` .

### Esempi

Mostra come aggiornare i tag dei documenti strutturati durante il salvataggio di un documento in PDF.

```csharp
Document doc = new Document();

// Inserisce un tag di documento strutturato con elenco a discesa.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// L'elenco a discesa mostra attualmente "Scegli un elemento" come testo predefinito.
// Imposta la proprietà "SelectedValue" su uno degli elementi dell'elenco a cui ottenere il tag
// mostra il valore dell'elemento dell'elenco invece del testo predefinito.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Crea un oggetto "PdfSaveOptions" da passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo salva il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "UpdateSdtContent" su "false" per non aggiornare i tag del documento strutturato
// durante il salvataggio del documento in PDF. Mostreranno i loro valori predefiniti come erano al momento della costruzione.
// Imposta la proprietà "UpdateSdtContent" su "true" per assicurarti che i tag visualizzino i valori aggiornati nel PDF.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../saveoptions/)
* assemblea [Aspose.Words](../../../)


