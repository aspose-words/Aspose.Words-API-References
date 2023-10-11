---
title: DocumentBuilder.MoveToCell
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Déplace le curseur vers une cellule du tableau dans la section actuelle.
type: docs
weight: 510
url: /fr/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Déplace le curseur vers une cellule du tableau dans la section actuelle.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tableIndex | Int32 | L'index de la table vers laquelle se déplacer. |
| rowIndex | Int32 | L'index de la ligne dans le tableau. |
| columnIndex | Int32 | L'index de la colonne dans le tableau. |
| characterIndex | Int32 | L'index du caractère à l'intérieur de la cellule. Une valeur négative permet de spécifier une position à partir de la fin de la cellule. Utilisez -1 pour passer à la fin de la cellule. |

### Remarques

La navigation s'effectue à l'intérieur de l'histoire en cours de la section en cours.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il spécifie un index from au début, 0 étant le premier élément. Lorsque l'index est inférieur à 0, il spécifie un index from à la fin, -1 étant le dernier élément.

### Exemples

Montre comment déplacer le curseur d’un générateur de documents vers une cellule d’un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une table 2x2 vide.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Parce que nous avons terminé le tableau avec la méthode EndTable,
// le curseur du générateur de document est actuellement en dehors de la table.
// Ce curseur a la même fonction que le curseur de texte clignotant de Microsoft Word.
// Il peut également être déplacé vers un emplacement différent dans le document à l'aide des méthodes MoveTo du générateur.
// Nous pouvons déplacer le curseur à l'intérieur du tableau vers une cellule spécifique.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


