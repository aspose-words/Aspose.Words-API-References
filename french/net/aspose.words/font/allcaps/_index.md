---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Police AllCaps. Formatez facilement votre texte en majuscules pour une meilleure lisibilité et un design percutant dans vos projets.
type: docs
weight: 10
url: /fr/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Vrai si la police est formatée en lettres majuscules.

```csharp
public bool AllCaps { get; set; }
```

## Exemples

Montre comment formater une exécution pour afficher son contenu en majuscules.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Il existe deux manières de faire en sorte qu'une exécution affiche son texte en minuscules en majuscules sans modifier le contenu.
// 1 - Définissez l'indicateur AllCaps pour afficher tous les caractères en majuscules normales :
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Définissez l'indicateur SmallCaps pour afficher tous les caractères en petites majuscules :
// Si un caractère est en minuscule, il apparaîtra en majuscule
// mais aura la même hauteur que les minuscules (la hauteur x de la police).
// Les caractères qui étaient en majuscules à l'origine auront le même aspect.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
