---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words per .NET API Reference
description: FieldOptions proprietà. Ottiene o imposta i percorsi dei modelli incorporati di MS Word.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Ottiene o imposta i percorsi dei modelli incorporati di MS Word.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### Osservazioni

Questa proprietà è utilizzata da[`FieldAutoText`](../../fieldautotext/) E[`FieldGlossary`](../../fieldglossary/) campi, se la voce di testo automatico di riferimento non viene trovata nel file[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) modello.

Per impostazione predefinita, MS Word memorizza i modelli integrati in c:\Users\&lt;nomeutente&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx e C:\Users\&lt;nomeutente&gt;\ File AppData\Roaming\Microsoft\Templates\Normal.dotm.

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

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldoptions/)
* assemblea [Aspose.Words](../../../)


