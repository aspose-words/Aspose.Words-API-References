---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: Cancella senza sforzo il contenuto del tag del tuo documento strutturato con il metodo Clear e mostra un segnaposto definito per una migliore gestione dei documenti.
type: docs
weight: 360
url: /it/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Cancella il contenuto di questo tag di documento strutturato e visualizza un segnaposto se definito.

```csharp
public void Clear()
```

## Osservazioni

Non è possibile cancellare il contenuto di un tag di documento strutturato se contiene revisioni.

Se questo tag di documento strutturato viene mappato su XML personalizzato (utilizzando il[`XmlMapping`](../xmlmapping/)proprietà ), il nodo XML referenziato viene cancellato.

## Esempi

Mostra come eliminare il contenuto degli elementi tag del documento strutturato.

```csharp
Document doc = new Document();

// Crea un tag di documento strutturato in testo normale e poi aggiungilo al documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Questo tag di documento strutturato, che si presenta sotto forma di casella di testo, visualizza già del testo segnaposto.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Crea un blocco di costruzione con contenuto di testo.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Imposta la proprietà "PlaceholderName" del tag del documento strutturato sul nome del nostro blocco di costruzione per ottenere
// il tag del documento strutturato per visualizzare il contenuto del blocco di costruzione al posto del testo predefinito originale.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Modifica il testo del tag del documento strutturato e nascondi il testo segnaposto.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Utilizzare il metodo "Clear" per cancellare il contenuto di questo tag di documento strutturato e visualizzare nuovamente il segnaposto.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
