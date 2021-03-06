---
title: MoveToField
second_title: Référence de l'API Aspose.Words pour .NET
description: Déplace le curseur vers un champ du document.
type: docs
weight: 510
url: /fr/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Déplace le curseur vers un champ du document.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| field | Field | Le champ vers lequel déplacer le curseur. |
| isAfter | Boolean | Si vrai, déplace le curseur après la fin du champ. Si faux, déplace le curseur avant le début du champ. |

### Exemples

Montre comment déplacer le curseur de point d'insertion de nœud d'un générateur de document vers un champ spécifique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ à l'aide de DocumentBuilder et ajoute une suite de texte après celui-ci.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Le curseur du constructeur est actuellement à la fin du document.
Assert.Null(builder.CurrentNode);

// Déplace le curseur vers le champ tout en spécifiant s'il faut placer ce curseur avant ou après le champ.
builder.MoveToField(field, moveCursorToAfterTheField);

// Notez que le curseur est en dehors du champ dans les deux cas.
// Cela signifie que nous ne pouvons pas modifier le champ à l'aide du générateur comme celui-ci.
// Pour modifier un champ, nous pouvons utiliser la méthode MoveTo du constructeur sur le FieldStart d'un champ
// ou nœud FieldSeparator pour placer le curseur à l'intérieur.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Voir également

* class [Field](../../../aspose.words.fields/field)
* class [DocumentBuilder](../../documentbuilder)
* espace de noms [Aspose.Words](../../documentbuilder)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
