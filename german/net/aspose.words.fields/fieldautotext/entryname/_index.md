---
title: FieldAutoText.EntryName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldAutoText eigendom. Ruft den Namen des AutoTextEintrags ab oder legt ihn fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

Ruft den Namen des AutoText-Eintrags ab oder legt ihn fest.

```csharp
public string EntryName { get; set; }
```

### Beispiele

Zeigt, wie ein Baustein mit den Feldern AUTOTEXT und GLOSSARY angezeigt wird.

```csharp
Document doc = new Document();

// Ein Glossardokument erstellen und einen AutoText-Baustein hinzufügen.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Erstelle eine Quelle und füge sie als Text zu unserem Baustein hinzu.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Legen Sie eine Datei fest, die Teile enthält, die unser Dokument oder die angehängte Vorlage möglicherweise nicht enthält.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten, Felder zum Anzeigen des Inhalts unseres Bausteins zu verwenden.
// 1 - Verwendung eines AUTOTEXT-Feldes:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Verwendung eines GLOSSARY-Felds:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Siehe auch

* class [FieldAutoText](../)
* namensraum [Aspose.Words.Fields](../../fieldautotext/)
* Montage [Aspose.Words](../../../)


