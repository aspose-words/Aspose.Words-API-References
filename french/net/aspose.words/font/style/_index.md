---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words pour .NET
description: Font Style propriété. Obtient ou définit le style de caractère appliqué à cette mise en forme en C#.
type: docs
weight: 400
url: /fr/net/aspose.words/font/style/
---
## Font.Style property

Obtient ou définit le style de caractère appliqué à cette mise en forme.

```csharp
public Style Style { get; set; }
```

## Exemples

Applique un double soulignement à toutes les exécutions d'un document formatées avec des styles de caractères personnalisés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un style personnalisé et l'applique au texte créé à l'aide d'un générateur de documents.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Parcourez chaque exécution et ajoutez un double soulignement à chaque style personnalisé.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
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
