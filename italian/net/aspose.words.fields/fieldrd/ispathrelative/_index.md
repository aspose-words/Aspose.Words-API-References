---
title: FieldRD.IsPathRelative
second_title: Aspose.Words per .NET API Reference
description: FieldRD proprietà. Ottiene o imposta se il percorso è relativo al documento corrente.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Ottiene o imposta se il percorso è relativo al documento corrente.

```csharp
public bool IsPathRelative { get; set; }
```

### Esempi

Mostra di utilizzare il campo RD per creare voci di sommario dalle intestazioni in altri documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Usa un generatore di documenti per inserire un sommario,
// e quindi aggiungi una voce per il sommario nella pagina seguente.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Inserisce un campo RD, che fa riferimento a un altro documento del file system locale nella sua proprietà FileName.
// Il sommario ora accetterà anche tutte le intestazioni del documento di riferimento come voci per la sua tabella.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = "ReferencedDocument.docx";
field.IsPathRelative = true;

Assert.AreEqual(" RD  ReferencedDocument.docx \\f", field.GetFieldCode());

 // Crea il documento a cui fa riferimento il campo RD e inserisci un'intestazione.
// Questa intestazione apparirà come una voce nel campo TOC nel nostro primo documento.
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
* spazio dei nomi [Aspose.Words.Fields](../../fieldrd/)
* assemblea [Aspose.Words](../../../)


