---
title: FieldAutoText.EntryName
second_title: Aspose.Words per .NET API Reference
description: FieldAutoText proprietà. Ottiene o imposta il nome della voce di glossario.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

Ottiene o imposta il nome della voce di glossario.

```csharp
public string EntryName { get; set; }
```

### Esempi

Mostra come visualizzare un blocco predefinito con campi TESTO AUTOMATICO e GLOSSARIO.

```csharp
Document doc = new Document();

// Crea un documento di glossario e vi aggiunge un blocco predefinito di glossario.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Crea una fonte e aggiungila come testo al nostro elemento costitutivo.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Imposta un file che contiene parti che il nostro documento o il modello allegato potrebbero non contenere.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per utilizzare i campi per visualizzare il contenuto del nostro blocco predefinito.
// 1 - Utilizzando un campo TESTO AUTOMATICO:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Utilizzando un campo GLOSSARIO:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Guarda anche

* class [FieldAutoText](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldautotext/)
* assemblea [Aspose.Words](../../../)


