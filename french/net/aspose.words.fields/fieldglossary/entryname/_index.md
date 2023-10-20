---
title: FieldGlossary.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words pour .NET
description: FieldGlossary EntryName propriété. Obtient ou définit le nom de lentrée de glossaire à insérer en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldglossary/entryname/
---
## FieldGlossary.EntryName property

Obtient ou définit le nom de l'entrée de glossaire à insérer.

```csharp
public string EntryName { get; set; }
```

## Exemples

Montre comment afficher un bloc de construction avec des champs AUTOTEXTE et GLOSSAIRE.

```csharp
Document doc = new Document();

// Créez un document glossaire et ajoutez-y un bloc de construction AutoTexte.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Créez une source et ajoutez-la sous forme de texte à notre bloc de construction.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Définit un fichier qui contient des parties que notre document ou son modèle joint ne peut pas contenir.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux façons d'utiliser les champs pour afficher le contenu de notre bloc de construction.
// 1 - Utilisation d'un champ AUTOTEXTE :
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Utilisation d'un champ GLOSSAIRE :
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Voir également

* class [FieldGlossary](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
