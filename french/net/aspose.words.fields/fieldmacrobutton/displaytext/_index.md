---
title: FieldMacroButton.DisplayText
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldMacroButton propriété. Obtient ou définit le texte devant apparaître comme le bouton sélectionné pour exécuter la macro ou la commande.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Obtient ou définit le texte devant apparaître comme le "bouton" sélectionné pour exécuter la macro ou la commande.

```csharp
public string DisplayText { get; set; }
```

### Exemples

Montre comment utiliser les champs MACROBUTTON pour nous permettre d'exécuter les macros d'un document en cliquant dessus.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Insère un champ MACROBUTTON et référence l'une des macros du document par son nom dans la propriété MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilisez la propriété pour référencer "ViewZoom200", une macro livrée avec Microsoft Word.
// Nous pouvons trouver toutes les autres macros via Affichage -> Macros (liste déroulante) -> Afficher les macros.
// Dans ce menu, sélectionnez "Word Commands" dans le menu déroulant "Macros in :".
// Si notre document contient une macro personnalisée portant le même nom qu'une macro stock,
// notre macro sera celle que le champ MACROBUTTON exécute.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Enregistre le document en tant que type de document prenant en charge les macros.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Voir également

* class [FieldMacroButton](../)
* espace de noms [Aspose.Words.Fields](../../fieldmacrobutton/)
* Assemblée [Aspose.Words](../../../)


