---
title: Font.StyleIdentifier
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Obtient ou définit lidentifiant de style indépendant des paramètres régionaux du style de caractère appliqué à cette mise en forme.
type: docs
weight: 410
url: /fr/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Obtient ou définit l'identifiant de style indépendant des paramètres régionaux du style de caractère appliqué à cette mise en forme.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Exemples

Montre comment modifier le style du texte existant.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières de référencer les styles.
// 1 - Utilisation du nom du style :
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Utilisation d'un identifiant de style intégré :
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Convertit toutes les utilisations d'un style en un autre,
// utilisant les méthodes ci-dessus pour référencer les anciens et les nouveaux styles.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Voir également

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


