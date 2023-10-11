---
title: FieldSubject.Text
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldSubject propriété. Obtient ou définit le texte du sujet.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Obtient ou définit le texte du sujet.

```csharp
public string Text { get; set; }
```

### Exemples

Montre comment utiliser le champ SUJET.

```csharp
Document doc = new Document();

// Définit une valeur pour la propriété intégrée "Sujet" du document.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Créez un champ SUBJECT pour afficher la valeur de cette propriété intégrée.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Si nous donnons la valeur de la propriété Texte du champ SUJET et que nous la mettons à jour, le champ
// écrase la valeur actuelle de la propriété intégrée "Sujet" par la valeur de sa propriété Text,
// puis affiche la nouvelle valeur.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Voir également

* class [FieldSubject](../)
* espace de noms [Aspose.Words.Fields](../../fieldsubject/)
* Assemblée [Aspose.Words](../../../)


