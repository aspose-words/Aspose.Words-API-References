---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Emplacement FieldGoToButton, définissez facilement des signets, des numéros de page ou des éléments pour une navigation fluide et une expérience utilisateur améliorée.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Obtient ou définit le nom d'un signet, un numéro de page ou un autre élément vers lequel accéder.

```csharp
public string Location { get; set; }
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
