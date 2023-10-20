---
title: StructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words per .NET
description: StructuredDocumentTag IsShowingPlaceholderText proprietà. Specifica se il contenuto di thisSDTdeve essere interpretato in modo da contenere testo segnaposto al contrario dei normali contenuti di testo allinterno dellSDT in C#.
type: docs
weight: 150
url: /it/net/aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/
---
## StructuredDocumentTag.IsShowingPlaceholderText property

Specifica se il contenuto di this**SDT**deve essere interpretato in modo da contenere testo segnaposto (al contrario dei normali contenuti di testo all'interno dell'SDT).

se impostato su`VERO` , questo stato verrà ripristinato (mostrando il testo segnaposto) all'apertura di questo documento.

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## Esempi

Mostra come utilizzare il contenuto di un blocco predefinito come testo segnaposto personalizzato per un tag di documento strutturato.

```csharp
Document doc = new Document();

// Inserisci un tag di documento strutturato in testo semplice del tipo "PlainText", che funzionerà come una casella di testo.
// Il contenuto che verrà visualizzato per impostazione predefinita è "Fai clic qui per inserire il testo". richiesta.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Possiamo fare in modo che il tag visualizzi il contenuto di un blocco predefinito invece del testo predefinito.
// Innanzitutto, aggiungi un elemento costitutivo con i contenuti al documento glossario.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Quindi, utilizza la proprietà "PlaceholderName" del tag del documento strutturato per fare riferimento a quel blocco predefinito per nome.
tag.PlaceholderName = "Custom Placeholder";

// Se "PlaceholderName" si riferisce a un blocco esistente nel documento glossario del documento principale,
// saremo in grado di verificare il building block tramite la proprietà "Placeholder".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Imposta la proprietà "IsShowingPlaceholderText" su "true" per trattare il
// contenuto corrente del tag del documento strutturato come testo segnaposto.
// Ciò significa che facendo clic sulla casella di testo in Microsoft Word verranno immediatamente evidenziati tutti i contenuti del tag.
// Imposta la proprietà "IsShowingPlaceholderText" su "false" per ottenere il file
// tag di documento strutturato per trattarne il contenuto come testo già inserito da un utente.
// Facendo clic su questo testo in Microsoft Word si posizionerà il cursore lampeggiante nella posizione cliccata.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
