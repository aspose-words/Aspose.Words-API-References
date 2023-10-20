---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words per .NET
description: StructuredDocumentTag IsTemporary proprietà. Specifica se questoSDT verrà rimosso dal documento WordProcessingML quando i suoi contenuti verranno modificati in C#.
type: docs
weight: 160
url: /it/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Specifica se questo**SDT** verrà rimosso dal documento WordProcessingML quando i suoi contenuti verranno modificati.

```csharp
public bool IsTemporary { get; set; }
```

## Esempi

Mostra come creare controlli monouso.

```csharp
Document doc = new Document();

// Inserisci un tag di documento strutturato in testo semplice,
// che fungerà da modulo di testo semplice in cui l'utente potrà inserire testo.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "IsTemporary" su "true" per far scomparire il tag del documento strutturato e
// assimila il suo contenuto nel documento dopo che l'utente lo ha modificato una volta in Microsoft Word.
// Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di modificare il contenuto
// del tag del documento strutturato un numero qualsiasi di volte.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Inserisci un altro tag di documento strutturato sotto forma di casella di controllo e imposta il suo stato predefinito su "selezionato".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Imposta la proprietà "IsTemporary" su "true" per far sì che la casella di controllo diventi un simbolo
// una volta che l'utente fa clic su di esso in Microsoft Word.
// Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di fare clic sulla casella di controllo un numero qualsiasi di volte.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
