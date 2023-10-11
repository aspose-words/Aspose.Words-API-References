---
title: FieldComments.Text
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldComments propriété. Obtient ou définit le texte des commentaires.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Obtient ou définit le texte des commentaires.

```csharp
public string Text { get; set; }
```

### Exemples

Montre comment utiliser le champ COMMENTAIRES.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définit une valeur pour la propriété intégrée "Commentaires" du document.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Créez un champ COMMENTAIRES pour afficher la valeur de cette propriété intégrée.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Si nous donnons la valeur de la propriété Text du champ COMMENTAIRES et la mettons à jour, le champ sera
// écrase la valeur actuelle de la propriété intégrée "Comments" par la valeur de sa propriété Text,
// puis affiche la nouvelle valeur.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Voir également

* class [FieldComments](../)
* espace de noms [Aspose.Words.Fields](../../fieldcomments/)
* Assemblée [Aspose.Words](../../../)


