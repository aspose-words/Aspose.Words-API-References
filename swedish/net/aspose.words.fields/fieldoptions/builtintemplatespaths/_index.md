---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words för .NET API Referens
description: FieldOptions fast egendom. Hämtar eller ställer in sökvägar för MS Words inbyggda mallar.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Hämtar eller ställer in sökvägar för MS Words inbyggda mallar.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### Anmärkningar

Den här egenskapen används av[`FieldAutoText`](../../fieldautotext/) och[`FieldGlossary`](../../fieldglossary/) fält, om refererad automatisk textinmatning inte finns i[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) mall.

Som standard lagrar MS Word inbyggda mallar i c:\Users\&lt;användarnamn&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx och C:\Users\&lt;användarnamn&gt;\ AppData\Roaming\Microsoft\Templates\Normal.dotm-filer.

### Exempel

Visar hur man visar ett byggblock med fälten AUTOTEXT och ORDLISTA.

```csharp
Document doc = new Document();

// Skapa ett ordlistadokument och lägg till ett autotextbyggblock till det.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Skapa en källa och lägg till den som text i vårt byggblock.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Ställ in en fil som innehåller delar som vårt dokument eller dess bifogade mall kanske inte innehåller.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två sätt att använda fält för att visa innehållet i vårt byggblock.
// 1 - Använda ett AUTOTEXT-fält:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Använda ett ORDLISTA-fält:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../fieldoptions/)
* hopsättning [Aspose.Words](../../../)


