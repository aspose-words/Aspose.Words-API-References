---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft Pfade von in MS Word integrierten Vorlagen ab oder legt sie fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Ruft Pfade von in MS Word integrierten Vorlagen ab oder legt sie fest.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### Bemerkungen

Diese Eigenschaft wird von der verwendet[`FieldAutoText`](../../fieldautotext/) und[`FieldGlossary`](../../fieldglossary/) Felder, wenn die referenzierte automatische Texteingabe nicht in der gefunden wird[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Schablone.

Standardmäßig speichert MS Word integrierte Vorlagen in c:\Users\&lt;Benutzername&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx and C:\Users\&lt;Benutzername&gt;\ AppData\Roaming\Microsoft\Templates\Normal.dotm-Dateien.

### Beispiele

Zeigt, wie ein Baustein mit AUTOTEXT- und GLOSSAR-Feldern angezeigt wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein Glossardokument und fügen Sie ihm einen AutoText-Baustein hinzu.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Erstellen Sie eine Quelle und fügen Sie sie unserem Baustein als Text hinzu.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Legen Sie eine Datei fest, die Teile enthält, die unser Dokument oder die angehängte Vorlage möglicherweise nicht enthält.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Im Folgenden finden Sie zwei Möglichkeiten, Felder zu verwenden, um den Inhalt unseres Bausteins anzuzeigen.
// 1 - Verwenden eines AUTOTEXT-Felds:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Verwenden eines GLOSSAR-Felds:
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


