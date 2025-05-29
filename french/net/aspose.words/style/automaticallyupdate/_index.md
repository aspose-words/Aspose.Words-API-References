---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété AutomaticallyUpdate améliore vos styles en les redéfinissant automatiquement pour une valeur et des performances optimales dans vos projets.
type: docs
weight: 20
url: /fr/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Remarques

Si la valeur de la propriété est définie sur true, MS Word redéfinit automatiquement le style actuel lorsque la mise en forme de paragraphe appropriée a été modifiée.

La propriété AutomaticallyUpdate s'applique uniquement aux styles de paragraphe.

La valeur par défaut est`FAUX`.

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
