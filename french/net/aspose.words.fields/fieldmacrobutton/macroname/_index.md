---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words pour .NET
description: FieldMacroButton MacroName propriété. Obtient ou définit le nom de la macro ou de la commande à exécuter en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

Obtient ou définit le nom de la macro ou de la commande à exécuter.

```csharp
public string MacroName { get; set; }
```

## Exemples

Montre comment utiliser les champs MACROBUTTON pour nous permettre d'exécuter les macros d'un document en cliquant.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Insère un champ MACROBUTTON et référence l'une des macros du document par son nom dans la propriété MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilisez la propriété pour référencer "ViewZoom200", une macro fournie avec Microsoft Word.
// On peut retrouver toutes les autres macros via View -> Macros (liste déroulante) -> Afficher les macros.
// Dans ce menu, sélectionnez "Commandes Word" dans la liste déroulante "Macros dans :".
// Si notre document contient une macro personnalisée portant le même nom qu'une macro stock,
// notre macro sera celle exécutée par le champ MACROBUTTON.
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
