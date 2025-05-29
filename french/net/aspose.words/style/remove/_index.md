---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: Supprimez facilement les styles indésirables de votre document grâce à la méthode « Supprimer les styles ». Améliorez l'apparence de votre contenu et préservez sa cohérence !
type: docs
weight: 230
url: /fr/net/aspose.words/style/remove/
---
## Style.Remove method

Supprime le style spécifié du document.

```csharp
public void Remove()
```

## Remarques

La suppression du style a les effets suivants sur le modèle de document :

* Toutes les références au style sont supprimées des paragraphes, séries et tableaux correspondants.
* Si le style de base est supprimé, sa mise en forme est déplacée vers les styles enfants.
* Si le style à supprimer a un style lié, alors les deux sont supprimés.

## Exemples

Montre comment créer et appliquer un style personnalisé.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Redéfinir automatiquement le style.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Appliquez l’un des styles du document au paragraphe que le générateur de documents est en train de créer.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Supprimez notre style personnalisé de la collection de styles du document.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Tout texte qui utilise un style supprimé revient à la mise en forme par défaut.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
