---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words per .NET
description: Scopri come la proprietà StructuredDocumentTag IsTemporary determina se il tuo SDT viene rimosso da WordProcessingML in caso di modifiche al contenuto. Ottimizza i tuoi documenti oggi stesso!
type: docs
weight: 160
url: /it/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Specifica se questo**SDT** verrà rimosso dal documento WordProcessingML quando il suo contenuto viene modificato.

```csharp
public bool IsTemporary { get; set; }
```

## Esempi

Mostra come realizzare controlli monouso.

```csharp
Document doc = new Document();

// Inserisci un tag di documento strutturato in testo normale,
// che fungerà da modulo di testo normale in cui l'utente potrà inserire del testo.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "IsTemporary" su "true" per far scomparire il tag del documento strutturato e
// assimilare il contenuto del documento dopo che l'utente lo ha modificato una volta in Microsoft Word.
// Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di modificare il contenuto
// del tag del documento strutturato un numero qualsiasi di volte.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Inserisce un altro tag di documento strutturato sotto forma di casella di controllo e imposta il suo stato predefinito su "selezionato".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Imposta la proprietà "IsTemporary" su "true" per far sì che la casella di controllo diventi un simbolo
// una volta che l'utente fa clic su di esso in Microsoft Word.
// Impostare la proprietà "IsTemporary" su "false" per consentire all'utente di fare clic sulla casella di controllo un numero qualsiasi di volte.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
