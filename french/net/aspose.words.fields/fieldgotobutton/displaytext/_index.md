---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words pour .NET
description: Personnalisez la propriété DisplayText de votre FieldGoToButton pour améliorer l'expérience utilisateur. Définissez facilement le texte du bouton pour une navigation fluide et un accès rapide.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Obtient ou définit le texte du « bouton » qui apparaît dans le document, de sorte qu'il puisse être sélectionné pour activer le saut.

```csharp
public string DisplayText { get; set; }
```

## Exemples

Affiche l'insertion d'un champ GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajouter un champ GOTOBUTTON. En double-cliquant sur ce champ dans Microsoft Word,
// il amènera le curseur de texte au signet dont le nom est référencé par la propriété Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Insérer un signet valide pour le champ à référencer.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Voir également

* class [FieldGoToButton](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
