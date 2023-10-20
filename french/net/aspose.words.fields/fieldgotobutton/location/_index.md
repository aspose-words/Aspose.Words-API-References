---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words pour .NET
description: FieldGoToButton Location propriété. Obtient ou définit le nom dun signet un numéro de page ou un autre élément auquel accéder en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Obtient ou définit le nom d'un signet, un numéro de page ou un autre élément auquel accéder.

```csharp
public string Location { get; set; }
```

## Exemples

Montre pour insérer un champ GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajout d'un champ GOTOBUTTON. Lorsque nous double-cliquons sur ce champ dans Microsoft Word,
// il amènera le curseur de texte vers le signet dont le nom fait référence à la propriété Location.
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
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
