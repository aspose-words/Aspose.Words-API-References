---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: Aspose.Words pour .NET
description: Naviguez sans effort dans votre document avec la méthode MoveToCell de DocumentBuilder, en positionnant rapidement le curseur dans n'importe quelle cellule du tableau pour une édition améliorée.
type: docs
weight: 540
url: /fr/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Déplace le curseur vers une cellule de tableau dans la section actuelle.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tableIndex | Int32 | L'index de la table vers laquelle se déplacer. |
| rowIndex | Int32 | L'index de la ligne dans la table. |
| columnIndex | Int32 | L'index de la colonne dans le tableau. |
| characterIndex | Int32 | L'index du caractère à l'intérieur de la cellule. Une valeur négative vous permet de spécifier une position à partir de la fin de la cellule. Utilisez -1 pour vous déplacer à la fin de la cellule. |

## Remarques

La navigation s'effectue à l'intérieur de l'histoire courante de la section courante.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il spécifie un index de début à partir de x000d, 0 étant le premier élément. Lorsque l'index est inférieur à 0, il spécifie un index de fin à partir de x000d, 1 étant le dernier élément.

## Exemples

Montre comment déplacer le curseur d'un générateur de documents vers une cellule d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une table 2x2 vide.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Parce que nous avons terminé le tableau avec la méthode EndTable,
// le curseur du générateur de documents est actuellement en dehors du tableau.
// Ce curseur a la même fonction que le curseur de texte clignotant de Microsoft Word.
// Il peut également être déplacé vers un autre emplacement dans le document à l'aide des méthodes MoveTo du générateur.
// Nous pouvons déplacer le curseur à l'intérieur du tableau vers une cellule spécifique.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
