---
title: FieldAdvance.DownOffset
linktitle: DownOffset
articleTitle: DownOffset
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldAdvance DownOffset, ajustez facilement le positionnement du texte avec un contrôle précis de l'espacement vertical pour une mise en forme améliorée du document.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldadvance/downoffset/
---
## FieldAdvance.DownOffset property

Obtient ou définit le nombre de points par lesquels le texte qui suit le champ doit être déplacé vers le bas.

```csharp
public string DownOffset { get; set; }
```

## Exemples

Montre comment insérer un champ ADVANCE et modifier ses propriétés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Vous trouverez ci-dessous deux manières d'utiliser le champ AVANCE pour ajuster la position du texte qui le suit.
// Les effets d'un champ AVANCE continuent d'être appliqués jusqu'à la fin du paragraphe,
// ou un autre champ ADVANCE met à jour les valeurs de décalage/coordonnées.
// 1 - Spécifiez un décalage directionnel :
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Déplacer le texte vers une position spécifiée par des coordonnées :
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Voir également

* class [FieldAdvance](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
