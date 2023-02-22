---
title: FieldKeywords.Text
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldKeywords propriété. Obtient ou définit le texte des motsclés.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Obtient ou définit le texte des mots-clés.

```csharp
public string Text { get; set; }
```

### Exemples

Indique d'insérer un champ KEYWORDS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez des mots-clés, également appelés "tags" dans l'explorateur de fichiers.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Le champ KEYWORDS affiche la valeur de cette propriété.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Définition d'une valeur pour la propriété Text du champ,
// puis la mise à jour du champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Voir également

* class [FieldKeywords](../)
* espace de noms [Aspose.Words.Fields](../../fieldkeywords/)
* Assemblée [Aspose.Words](../../../)


