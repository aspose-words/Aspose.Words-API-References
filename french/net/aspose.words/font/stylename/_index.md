---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font StyleName, gérez facilement les styles de caractères pour une mise en forme de texte améliorée et une flexibilité de conception dans vos projets.
type: docs
weight: 430
url: /fr/net/aspose.words/font/stylename/
---
## Font.StyleName property

Obtient ou définit le nom du style de caractère appliqué à cette mise en forme.

```csharp
public string StyleName { get; set; }
```

## Exemples

Montre comment modifier le style d'un texte existant.

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

// Convertir toutes les utilisations d'un style en un autre,
// en utilisant les méthodes ci-dessus pour référencer les anciens et les nouveaux styles.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
