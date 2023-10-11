---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft Pfade der in MS Word integrierten Vorlagen ab oder legt diese fest.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Ruft Pfade der in MS Word integrierten Vorlagen ab oder legt diese fest.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### Bemerkungen

Diese Eigenschaft wird von verwendet[`FieldAutoText`](../../fieldautotext/) Und[`FieldGlossary`](../../fieldglossary/) Felder, wenn der referenzierte automatische Texteintrag nicht im gefunden wird[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Vorlage.

Standardmäßig speichert MS Word integrierte Vorlagen in c:\Benutzer\&lt;Benutzername&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx und C:\Benutzer\&lt;Benutzername&gt;\ AppData\Roaming\Microsoft\Templates\Normal.dotm-Dateien.

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

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


