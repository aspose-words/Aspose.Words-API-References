---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words per .NET
description: Scopri come gestire i percorsi dei modelli predefiniti di MS Word con la proprietà BuiltInTemplatesPaths di FieldOptions per una creazione di documenti senza interruzioni.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Ottiene o imposta i percorsi dei modelli incorporati di MS Word.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## Osservazioni

Questa proprietà è utilizzata da[`FieldAutoText`](../../fieldautotext/) E[`FieldGlossary`](../../fieldglossary/) campi, se l'immissione di testo automatico referenziata non viene trovata nel[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) modello.

Per impostazione predefinita, MS Word memorizza i modelli incorporati nei file c:\Users\&lt;nomeutente&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx e C:\Users\&lt;nomeutente&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm.

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

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
