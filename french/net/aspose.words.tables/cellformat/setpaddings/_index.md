---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words pour .NET
description: Découvrez la méthode CellFormat SetPaddings pour personnaliser l'espacement des cellules en points, améliorant ainsi votre mise en page pour une meilleure lisibilité et une meilleure conception.
type: docs
weight: 170
url: /fr/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Définit la quantité d'espace (en points) à ajouter à gauche/en haut/à droite/en bas du contenu de la cellule.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Exemples

Montre comment remplir le contenu d'une cellule avec des espaces.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez une distance de remplissage (en points) entre la bordure et le contenu du texte
 // de chaque cellule de tableau que nous créons avec le générateur de documents.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Créez un tableau avec une cellule dont le contenu sera rempli d'espaces.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Voir également

* class [CellFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
