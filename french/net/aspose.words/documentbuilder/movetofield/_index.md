---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words pour .NET
description: Naviguez sans effort dans vos documents avec la méthode MoveToField de DocumentBuilder, permettant un déplacement rapide du curseur vers n'importe quel champ pour une efficacité d'édition améliorée.
type: docs
weight: 570
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
| isAfter | Boolean | Quand`vrai` , déplace le curseur pour qu'il soit après la fin du champ. Lorsque`FAUX`, déplace le curseur avant le début du champ. |

## Exemples

Montre comment déplacer le curseur du point d'insertion du nœud d'un générateur de documents vers un champ spécifique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un champ à l'aide de DocumentBuilder et ajoutez une série de texte après celui-ci.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Le curseur du constructeur est actuellement à la fin du document.
Assert.Null(builder.CurrentNode);

// Déplacez le curseur vers le champ tout en spécifiant si vous souhaitez placer ce curseur avant ou après le champ.
builder.MoveToField(field, moveCursorToAfterTheField);

// Notez que le curseur est en dehors du champ dans les deux cas.
// Cela signifie que nous ne pouvons pas modifier le champ en utilisant le générateur comme ceci.
// Pour éditer un champ, nous pouvons utiliser la méthode MoveTo du générateur sur le FieldStart d'un champ
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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
