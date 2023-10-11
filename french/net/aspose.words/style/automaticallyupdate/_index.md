---
title: Style.AutomaticallyUpdate
second_title: Référence de l'API Aspose.Words pour .NET
description: Style propriété. Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée.
type: docs
weight: 20
url: /fr/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

### Remarques

Si la valeur de la propriété est définie sur true, MS Word redéfinit automatiquement le style actuel lorsque le formatage de paragraphe approprié a été modifié.

La propriété AutomaticallyUpdate s’applique uniquement aux styles de paragraphe.

La valeur par défaut est`FAUX`.

### Exemples

Montre comment créer et appliquer un style personnalisé.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Redéfinit automatiquement le style.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Applique l'un des styles du document au paragraphe créé par le générateur de document.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Supprimez notre style personnalisé de la collection de styles du document.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Tout texte utilisant un style supprimé revient au formatage par défaut.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../style/)
* Assemblée [Aspose.Words](../../../)


