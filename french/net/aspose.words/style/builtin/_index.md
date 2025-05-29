---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words pour .NET
description: Découvrez si un style est une option intégrée à MS Word. Améliorez la conception de vos documents grâce à notre guide complet sur les styles intégrés de Word !
type: docs
weight: 40
url: /fr/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Vrai si ce style est l'un des styles intégrés dans MS Word.

```csharp
public bool BuiltIn { get; }
```

## Exemples

Montre comment différencier les styles personnalisés des styles intégrés.

```csharp
Document doc = new Document();

// Lorsque nous créons un document à l'aide de Microsoft Word ou par programmation à l'aide d'Aspose.Words,
// le document sera accompagné d'une collection de styles à appliquer à son texte pour modifier son apparence.
// Nous pouvons accéder à ces styles intégrés via la collection « Styles » du document.
// Ces styles auront tous l'indicateur « BuiltIn » défini sur « true ».
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Créez un style personnalisé et ajoutez-le à la collection.
 // Les styles personnalisés tels que celui-ci auront l'indicateur « BuiltIn » défini sur « false ».
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
