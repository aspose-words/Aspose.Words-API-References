---
title: FieldAutoText.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldAutoText EntryName“, um AutoText-Eintragsnamen einfach zu verwalten und so die Automatisierung und Effizienz Ihrer Dokumente zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

Ruft den Namen des AutoText-Eintrags ab oder legt ihn fest.

```csharp
public string EntryName { get; set; }
```

## Beispiele

Zeigt, wie ein Baustein mit AUTOTEXT- und GLOSSAR-Feldern angezeigt wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein Glossardokument und fügen Sie einen AutoText-Baustein hinzu.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Erstellen Sie eine Quelle und fügen Sie sie als Text zu unserem Baustein hinzu.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Legen Sie eine Datei fest, die Teile enthält, die in unserem Dokument oder der angehängten Vorlage möglicherweise nicht enthalten sind.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten, Felder zum Anzeigen des Inhalts unseres Bausteins zu verwenden.
// 1 - Verwenden eines AUTOTEXT-Feldes:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Verwenden eines GLOSSAR-Feldes:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Siehe auch

* class [FieldAutoText](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
