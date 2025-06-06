---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer les chemins de modèles intégrés de MS Word avec la propriété FieldOptions BuiltInTemplatesPaths pour une création de documents transparente.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Obtient ou définit les chemins des modèles intégrés de MS Word.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## Remarques

Cette propriété est utilisée par le[`FieldAutoText`](../../fieldautotext/) et[`FieldGlossary`](../../fieldglossary/) champs, si l'entrée de texte automatique référencée n'est pas trouvée dans le[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) modèle.

Par défaut, MS Word stocke les modèles intégrés dans les fichiers c:\Users\&lt;username&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx et C:\Users\&lt;username&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm.

## Exemples

Montre comment afficher un bloc de construction avec les champs AUTOTEXT et GLOSSAIRE.

```csharp
Document doc = new Document();

// Créez un document de glossaire et ajoutez-y un bloc de construction AutoText.
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

// Définissez un fichier qui contient des parties que notre document ou son modèle joint ne peuvent pas contenir.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'utiliser des champs pour afficher le contenu de notre bloc de construction.
// 1 - Utilisation d'un champ AUTOTEXT :
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

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
