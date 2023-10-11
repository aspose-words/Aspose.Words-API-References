---
title: DocumentBuilder.MoveToParagraph
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Déplace le curseur vers un paragraphe de la section actuelle.
type: docs
weight: 570
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
| characterIndex | Int32 | L'index du caractère à l'intérieur du paragraphe. Une valeur négative permet de spécifier une position à partir de la fin du paragraphe. Utilisez -1 pour passer à la fin de le paragraphe. |

### Remarques

La navigation s'effectue à l'intérieur de l'histoire actuelle de la section actuelle. Autrement dit, si vous avez déplacé le curseur vers l'en-tête principal de la première section, alors*paragraphIndex*spécifié l'index du paragraphe à l'intérieur de ce header de cette section.

Quand*paragraphIndex* est supérieur ou égal à 0, il spécifie un index depuis le début de la section, 0 étant le premier paragraphe. Quand*paragraphIndex* est inférieur à 0, , il a spécifié un index à partir de la fin de la section, -1 étant le dernier paragraphe.

### Exemples

Montre comment déplacer la position du curseur d'un générateur vers un paragraphe spécifié.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Créez un générateur de document pour modifier le document. Le curseur du constructeur,
// quel est le point où il insérera de nouveaux nœuds lorsque nous appellerons ses méthodes de construction de documents,
// se trouve actuellement au début du document.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Déplacer ce curseur vers un autre paragraphe placera ce curseur devant ce paragraphe.
builder.MoveToParagraph(2, 0);
// Tout nouveau contenu que nous ajoutons sera inséré à ce stade.
builder.Writeln("This is a new third paragraph. ");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


