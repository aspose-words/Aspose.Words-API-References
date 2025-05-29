---
title: StructuredDocumentTag.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: Aspose.Words per .NET
description: Scopri la proprietà StructuredDocumentTag PlaceholderName per gestire facilmente i nomi dei BuildingBlock e migliorare il testo segnaposto del tuo documento.
type: docs
weight: 240
url: /it/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

Ottiene o imposta il nome del[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto.

```csharp
public string PlaceholderName { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidOperationException | Genera se BuildingBlock ha questo nome[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) non è presente in[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/). |

## Esempi

Mostra come utilizzare il contenuto di un blocco di costruzione come testo segnaposto personalizzato per un tag di documento strutturato.

```csharp
Document doc = new Document();

// Inserire un tag di documento strutturato in testo normale di tipo "PlainText", che funzionerà come una casella di testo.
// Per impostazione predefinita, il contenuto visualizzato è un prompt "Fai clic qui per immettere il testo".
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Possiamo far sì che il tag visualizzi il contenuto di un blocco di costruzione anziché il testo predefinito.
// Per prima cosa, aggiungi un blocco di costruzione con contenuti al documento del glossario.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Quindi, utilizzare la proprietà "PlaceholderName" del tag del documento strutturato per fare riferimento a quel blocco di costruzione tramite il nome.
tag.PlaceholderName = "Custom Placeholder";

// Se "PlaceholderName" fa riferimento a un blocco esistente nel documento glossario del documento padre,
// saremo in grado di verificare il blocco di costruzione tramite la proprietà "Segnaposto".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Imposta la proprietà "IsShowingPlaceholderText" su "true" per trattare il
// contenuto corrente del tag del documento strutturato come testo segnaposto.
// Ciò significa che cliccando sulla casella di testo in Microsoft Word verrà immediatamente evidenziato tutto il contenuto del tag.
// Imposta la proprietà "IsShowingPlaceholderText" su "false" per ottenere il
// tag del documento strutturato per trattare il suo contenuto come testo già inserito dall'utente.
// Facendo clic su questo testo in Microsoft Word, il cursore lampeggiante verrà posizionato nel punto cliccato.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
