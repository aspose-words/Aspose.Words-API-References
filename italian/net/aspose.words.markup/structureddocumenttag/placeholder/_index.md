---
title: StructuredDocumentTag.Placeholder
linktitle: Placeholder
articleTitle: Placeholder
second_title: Aspose.Words per .NET
description: StructuredDocumentTag Placeholder proprietà. Ottiene il fileBuildingBlockcontenente testo segnaposto che dovrebbe essere visualizzato quando i contenuti dellesecuzione di questo SDT sono vuoti lelemento XML mappato associato è vuoto come specificato tramiteXmlMapping element o ilIsShowingPlaceholderText lelemento èVERO  in C#.
type: docs
weight: 230
url: /it/net/aspose.words.markup/structureddocumenttag/placeholder/
---
## StructuredDocumentTag.Placeholder property

Ottiene il file[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)contenente testo segnaposto che dovrebbe essere visualizzato quando i contenuti dell'esecuzione di questo SDT sono vuoti, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](../xmlmapping/) element o il[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) l'elemento è`VERO` .

```csharp
public BuildingBlock Placeholder { get; }
```

## Osservazioni

Può essere`nullo`, il che significa che il segnaposto non è applicabile per questo Sdt.

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

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
