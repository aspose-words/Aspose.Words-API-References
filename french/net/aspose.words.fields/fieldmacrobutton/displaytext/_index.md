---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser la propriété DisplayText du FieldMacroButton pour une exécution optimisée des macros. Définissez le texte de bouton idéal pour des commandes utilisateur fluides !
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Obtient ou définit le texte à afficher comme le « bouton » sélectionné pour exécuter la macro ou la commande.

```csharp
public string DisplayText { get; set; }
```

## Exemples

Montre comment utiliser les champs MACROBUTTON pour nous permettre d'exécuter les macros d'un document en cliquant.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Insérez un champ MACROBUTTON et référencez l'une des macros du document par son nom dans la propriété MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilisez la propriété pour référencer « ViewZoom200 », une macro fournie avec Microsoft Word.
// Nous pouvons trouver toutes les autres macros via Affichage -> Macros (liste déroulante) -> Afficher les macros.
// Dans ce menu, sélectionnez « Commandes Word » dans la liste déroulante « Macros dans : ».
// Si notre document contient une macro personnalisée portant le même nom qu'une macro standard,
// notre macro sera celle que le champ MACROBUTTON exécute.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Enregistrez le document en tant que type de document prenant en charge les macros.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Voir également

* class [FieldMacroButton](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
