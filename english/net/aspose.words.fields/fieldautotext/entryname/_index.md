---
title: FieldAutoText.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words for .NET
description: FieldAutoText EntryName property. Gets or sets the name of the AutoText entry in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

Gets or sets the name of the AutoText entry.

```csharp
public string EntryName { get; set; }
```

## Examples

Shows how to display a building block with AUTOTEXT and GLOSSARY fields.

```csharp
Document doc = new Document();

// Create a glossary document and add an AutoText building block to it.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Create a source and add it as text to our building block.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Set a file which contains parts that our document, or its attached template may not contain.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways to use fields to display the contents of our building block.
// 1 -  Using an AUTOTEXT field:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 -  Using a GLOSSARY field:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### See Also

* class [FieldAutoText](../)
* namespace [Aspose.Words.Fields](../../fieldautotext/)
* assembly [Aspose.Words](../../../)
