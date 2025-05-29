---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie integrierte MS Word-Vorlagenpfade mit der FieldOptions BuiltInTemplatesPaths-Eigenschaft für eine nahtlose Dokumenterstellung verwalten.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Ruft die Pfade der in MS Word integrierten Vorlagen ab oder legt sie fest.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird verwendet von[`FieldAutoText`](../../fieldautotext/) Und[`FieldGlossary`](../../fieldglossary/) Felder, wenn die referenzierte automatische Texteingabe nicht in der[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Vorlage.

Standardmäßig speichert MS Word integrierte Vorlagen in den Dateien c:\Users\&lt;Benutzername&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx und C:\Users\&lt;Benutzername&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm.

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

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
