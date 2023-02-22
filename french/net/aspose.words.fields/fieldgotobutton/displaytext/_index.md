---
title: FieldGoToButton.DisplayText
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldGoToButton propriété. Obtient ou définit le texte du bouton qui apparaît dans le document de sorte quil peut être sélectionné pour activer le saut.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Obtient ou définit le texte du "bouton" qui apparaît dans le document, de sorte qu'il peut être sélectionné pour activer le saut.

```csharp
public string DisplayText { get; set; }
```

### Exemples

Indique d'insérer un champ GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoute un champ GOTOBUTTON. Lorsque nous double-cliquons sur ce champ dans Microsoft Word,
// il amènera le curseur de texte au signet dont le nom fait référence à la propriété Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Insère un signet valide pour le champ à référencer.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Voir également

* class [FieldGoToButton](../)
* espace de noms [Aspose.Words.Fields](../../fieldgotobutton/)
* Assemblée [Aspose.Words](../../../)


