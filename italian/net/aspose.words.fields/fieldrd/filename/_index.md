---
title: FieldRD.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FileName di FieldRD semplifica la gestione dei file impostando facilmente i nomi per generare i tuoi sommari e indici.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

Ottiene o imposta il nome del file da includere durante la generazione di un indice, di una tabella delle autorità o di un indice.

```csharp
public string FileName { get; set; }
```

## Esempi

Mostra come utilizzare il campo RD per creare voci di indice a partire da intestazioni di altri documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizzare un generatore di documenti per inserire un indice,
// e quindi aggiungere una voce per l'indice nella pagina seguente.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Inserire un campo RD che fa riferimento a un altro documento del file system locale nella sua proprietà FileName.
// L'indice accetterà ora anche tutte le intestazioni del documento a cui si fa riferimento come voci per la sua tabella.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Crea il documento a cui fa riferimento il campo RD e inserisci un'intestazione.
// Questa intestazione verrà visualizzata come voce nel campo TOC del nostro primo documento.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Guarda anche

* class [FieldRD](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
