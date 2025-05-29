---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Gérez facilement vos FieldKeywords ! Accédez au texte de vos mots-clés et personnalisez-le pour des performances SEO optimales et une visibilité accrue.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Obtient ou définit le texte des mots-clés.

```csharp
public string Text { get; set; }
```

## Exemples

Affiche l'insertion d'un champ MOTS CLÉS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez quelques mots-clés, également appelés « balises » dans l'Explorateur de fichiers.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Le champ MOTS CLÉS affiche la valeur de cette propriété.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Définition d'une valeur pour la propriété Texte du champ,
// et la mise à jour du champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Voir également

* class [FieldKeywords](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
