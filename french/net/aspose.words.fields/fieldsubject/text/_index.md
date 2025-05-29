---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Gérez la propriété Texte du sujet du champ sans effort : obtenez ou définissez votre texte d'objet pour une gestion transparente des données et une expérience utilisateur améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Obtient ou définit le texte du sujet.

```csharp
public string Text { get; set; }
```

## Exemples

Montre comment utiliser le champ SUJET.

```csharp
Document doc = new Document();

// Définissez une valeur pour la propriété intégrée « Sujet » du document.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Créez un champ SUBJECT pour afficher la valeur de cette propriété intégrée.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Si nous donnons la valeur de la propriété Texte du champ SUBJECT et la mettons à jour, le champ sera
// remplacer la valeur actuelle de la propriété intégrée « Subject » par la valeur de sa propriété Text,
// puis affichez la nouvelle valeur.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Voir également

* class [FieldSubject](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
