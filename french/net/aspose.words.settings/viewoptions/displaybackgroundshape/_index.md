---
title: ViewOptions.DisplayBackgroundShape
second_title: Référence de l'API Aspose.Words pour .NET
description: ViewOptions propriété. Contrôle laffichage de la forme darrièreplan en mode dimpression.
type: docs
weight: 10
url: /fr/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Contrôle l'affichage de la forme d'arrière-plan en mode d'impression.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

### Exemples

Montre comment masquer/afficher les images d'arrière-plan du document dans les options d'affichage.

```csharp
// Utilisez une chaîne HTML pour créer un nouveau document avec une couleur d'arrière-plan plate.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// La source du document a un arrière-plan de couleur unie,
// dont la présence définira le drapeau "DisplayBackgroundShape" sur "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Conservez "DisplayBackgroundShape" sur "true" pour que le document affiche la couleur d'arrière-plan.
// Cela peut affecter certaines couleurs de texte pour améliorer la visibilité.
// Définissez "DisplayBackgroundShape" sur "false" pour ne pas afficher la couleur d'arrière-plan.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Voir également

* class [ViewOptions](../)
* espace de noms [Aspose.Words.Settings](../../viewoptions/)
* Assemblée [Aspose.Words](../../../)


