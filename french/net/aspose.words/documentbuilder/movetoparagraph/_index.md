---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words pour .NET
description: Naviguez sans effort dans votre document avec la méthode MoveToParagraph de DocumentBuilder, permettant un déplacement rapide du curseur vers n'importe quel paragraphe de votre section.
type: docs
weight: 600
url: /fr/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Déplace le curseur vers un paragraphe de la section actuelle.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| paragraphIndex | Int32 | L'index du paragraphe vers lequel se déplacer. |
| characterIndex | Int32 | L'index du caractère à l'intérieur du paragraphe. Une valeur négative vous permet de spécifier une position à partir de la fin du paragraphe. Utilisez -1 pour vous déplacer à la fin du paragraphe. |

## Remarques

La navigation s'effectue à l'intérieur de l'histoire actuelle de la section actuelle. Autrement dit, si vous avez déplacé le curseur vers l'en-tête principal de la première section, alors*paragraphIndex* spécifié l'index du paragraphe à l'intérieur de cet en-tête de cette section.

Quand*paragraphIndex* est supérieur ou égal à 0, il spécifie un index à partir de le début de la section, 0 étant le premier paragraphe.*paragraphIndex* est inférieur à 0, il a spécifié un index à partir de la fin de la section avec -1 étant le dernier paragraphe.

## Exemples

Montre comment déplacer la position du curseur d'un générateur vers un paragraphe spécifié.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Créer un générateur de documents pour modifier le document. Le curseur du générateur,
// qui est le point où il insérera de nouveaux nœuds lorsque nous appellerons ses méthodes de construction de documents,
// est actuellement au début du document.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Déplacer ce curseur vers un autre paragraphe placera ce curseur devant ce paragraphe.
builder.MoveToParagraph(2, 0);
// Tout nouveau contenu que nous ajoutons sera inséré à ce stade.
builder.Writeln("This is a new third paragraph. ");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
