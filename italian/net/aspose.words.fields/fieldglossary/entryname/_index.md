---
title: FieldGlossary.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldGlossary EntryName per gestire facilmente le voci del glossario ottieni o imposta nomi per un'integrazione fluida dei contenuti.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldglossary/entryname/
---
## FieldGlossary.EntryName property

Ottiene o imposta il nome della voce del glossario da inserire.

```csharp
public string EntryName { get; set; }
```

## Esempi

Mostra come visualizzare un blocco di costruzione con i campi AUTOTEXT e GLOSSARY.

```csharp
Document doc = new Document();

// Crea un documento di glossario e aggiungigli un blocco di testo automatico.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Creiamo una sorgente e aggiungila come testo al nostro blocco di costruzione.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Imposta un file che contiene parti che il nostro documento o il modello allegato potrebbero non contenere.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per utilizzare i campi per visualizzare il contenuto del nostro blocco di costruzione.
// 1 - Utilizzo di un campo AUTOTEXT:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Utilizzo di un campo GLOSSARIO:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Guarda anche

* class [FieldGlossary](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
