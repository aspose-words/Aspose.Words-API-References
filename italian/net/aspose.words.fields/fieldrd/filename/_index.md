---
title: FieldRD.FileName
second_title: Aspose.Words per .NET API Reference
description: FieldRD proprietà. Ottiene o imposta il nome del file da includere durante la generazione di un sommario un indice delle autorità o un indice.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

Ottiene o imposta il nome del file da includere durante la generazione di un sommario, un indice delle autorità o un indice.

```csharp
public string FileName { get; set; }
```

### Esempi

Mostra come utilizzare il campo RD per creare voci di sommario da intestazioni di altri documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un generatore di documenti per inserire un sommario,
// e poi aggiungi una voce per il sommario nella pagina seguente.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Inserisci un campo RD, che fa riferimento a un altro documento del file system locale nella relativa proprietà FileName.
// Il sommario ora accetterà anche tutti i titoli del documento di riferimento come voci per la sua tabella.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Crea il documento a cui fa riferimento il campo RD e inserisce un'intestazione.
// Questa intestazione verrà visualizzata come voce nel campo TOC nel nostro primo documento.
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


