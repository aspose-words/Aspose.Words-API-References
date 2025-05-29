---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété Style de police pour personnaliser les styles de caractères dans votre mise en forme pour améliorer l'attrait et la lisibilité du texte.
type: docs
weight: 410
url: /fr/net/aspose.words/font/style/
---
## Font.Style property

Obtient ou définit le style de caractère appliqué à cette mise en forme.

```csharp
public Style Style { get; set; }
```

## Exemples

Applique un double soulignement à toutes les exécutions d'un document qui sont formatées avec des styles de caractères personnalisés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un style personnalisé et appliquez-le au texte créé à l'aide d'un générateur de documents.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Itérez sur chaque exécution et ajoutez un double soulignement à chaque style personnalisé.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### Voir également

* class [Style](../../style/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
