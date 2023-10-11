---
title: StructuredDocumentTag.Id
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Specifica un ID numerico persistente univoco di sola lettura per questo SDT.
type: docs
weight: 140
url: /it/net/aspose.words.markup/structureddocumenttag/id/
---
## StructuredDocumentTag.Id property

Specifica un ID numerico persistente univoco di sola lettura per questo **SDT**.

```csharp
public int Id { get; }
```

### Osservazioni

L'attributo ID deve seguire queste regole:

* Il documento conserverà gli ID SDT solo se l'intero documento viene clonato[`Clone`](../../../aspose.words/document/clone/).
* Durante[`ImportNode`](../../../aspose.words/documentbase/importnode/) L'ID verrà mantenuto se l'importazione non causa conflitti con altri ID SDT nel documento di destinazione.
* Se più nodi SDT specificano lo stesso valore del numero decimale per l'attributo Id, , il primo SDT nel documento manterrà questo Id originale, e a tutti i successivi nodi SDT verranno assegnati nuovi identificatori quando il documento verrà caricato.
* Durante l'SDT autonomoINodeCloningListener) operazione verrà generato un nuovo ID univoco per il nodo SDT clonato.
* Se Id non è specificato nel documento di origine, al nodo SDT verrà assegnato un nuovo identificatore univoco quando il documento viene caricato.

### Esempi

Mostra come creare un tag di documento strutturato in una casella di testo semplice e modificarne l'aspetto.

```csharp
Document doc = new Document();

// Crea un tag di documento strutturato che conterrà testo semplice.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta il titolo e il colore della cornice che appare quando passi il mouse sul tag del documento strutturato in Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Imposta un tag per questo tag di documento strutturato, che è ottenibile
// come elemento XML denominato "tag", con la stringa seguente nel suo attributo "@val".
tag.Tag = "MyPlainTextSDT";

// Ogni tag di documento strutturato ha un ID univoco casuale.
Assert.That(tag.Id, Is.Positive);

// Imposta il carattere per il testo all'interno del tag del documento strutturato.
tag.ContentsFont.Name = "Arial";

// Imposta il carattere per il testo alla fine del tag del documento strutturato.
// Qualsiasi testo digitato nel corpo del documento dopo essere usciti dal tag con i tasti freccia utilizzerà questo carattere.
tag.EndCharacterFont.Name = "Arial Black";

// Per impostazione predefinita, questo è falso e premere Invio all'interno di un tag di documento strutturato non fa nulla.
// Se impostato su true, il tag del nostro documento strutturato può avere più righe.

// Imposta la proprietà "Multiline" su "false" per consentire solo il contenuto
// di questo tag di documento strutturato su una singola riga.
// Imposta la proprietà "Multiline" su "true" per consentire al tag di contenere più righe di contenuto.
tag.Multiline = true;

// Imposta la proprietà "Appearance" su "SdtAppearance.Tags" per mostrare i tag attorno al contenuto.
 // Per impostazione predefinita, il tag del documento strutturato viene visualizzato come BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Inserisci un clone del nostro tag di documento strutturato in un nuovo paragrafo.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Utilizza il metodo "RemoveSelfOnly" per rimuovere un tag di documento strutturato, mantenendone il contenuto nel documento.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


