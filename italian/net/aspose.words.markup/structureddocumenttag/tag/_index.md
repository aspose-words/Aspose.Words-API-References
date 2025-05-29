---
title: StructuredDocumentTag.Tag
linktitle: Tag
articleTitle: Tag
second_title: Aspose.Words per .NET
description: Scopri la proprietà StructuredDocumentTag che definisce i tag essenziali per i nodi SDT, garantendo un'organizzazione e una gestione efficiente dei documenti.
type: docs
weight: 280
url: /it/net/aspose.words.markup/structureddocumenttag/tag/
---
## StructuredDocumentTag.Tag property

Specifica un tag associato al nodo SDT corrente. Non può essere`null` .

```csharp
public string Tag { get; set; }
```

## Osservazioni

Un tag è una stringa arbitraria che le applicazioni possono associare a SDT per identificarlo senza fornire un nome descrittivo visibile.

## Esempi

Mostra come creare un tag di documento strutturato in una casella di testo normale e modificarne l'aspetto.

```csharp
Document doc = new Document();

// Crea un tag di documento strutturato che conterrà testo normale.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta il titolo e il colore della cornice che appare quando passi il mouse sopra il tag del documento strutturato in Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Imposta un tag per questo tag del documento strutturato, che è ottenibile
// come un elemento XML denominato "tag", con la stringa sottostante nel suo attributo "@val".
tag.Tag = "MyPlainTextSDT";

// Ogni tag di documento strutturato ha un ID univoco casuale.
Assert.IsTrue(tag.Id > 0);

// Imposta il font per il testo all'interno del tag del documento strutturato.
tag.ContentsFont.Name = "Arial";

// Imposta il font per il testo alla fine del tag del documento strutturato.
// Qualsiasi testo digitato nel corpo del documento dopo essere usciti dal tag con i tasti freccia utilizzerà questo font.
tag.EndCharacterFont.Name = "Arial Black";

// Per impostazione predefinita, questo valore è falso e premendo Invio mentre ci si trova all'interno di un tag di documento strutturato non accade nulla.
// Se impostato su true, il tag del documento strutturato può contenere più righe.

// Imposta la proprietà "Multiline" su "false" per consentire solo il contenuto
// di questo tag di documento strutturato in modo che si estenda su una singola riga.
// Impostare la proprietà "Multiline" su "true" per consentire al tag di contenere più righe di contenuto.
tag.Multiline = true;

// Imposta la proprietà "Aspetto" su "SdtAppearance.Tags" per mostrare i tag attorno al contenuto.
 // Per impostazione predefinita, il tag del documento strutturato viene visualizzato come BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Inseriamo un clone del nostro tag documento strutturato in un nuovo paragrafo.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Utilizzare il metodo "RemoveSelfOnly" per rimuovere un tag di documento strutturato, mantenendone il contenuto nel documento.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
