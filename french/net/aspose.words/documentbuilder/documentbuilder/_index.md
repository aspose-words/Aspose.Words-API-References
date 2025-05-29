---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words pour .NET
description: Créez des documents performants en toute simplicité avec DocumentBuilder. Initialisez une nouvelle instance et optimisez la gestion de vos documents dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Initialise une nouvelle instance de cette classe.

```csharp
public DocumentBuilder()
```

## Remarques

Crée un nouveau[`DocumentBuilder`](../)objet et l'attache à un nouveau[`Document`](../../document/) objet.

## Exemples

Montre comment insérer du texte formaté à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez le formatage de la police, puis ajoutez du texte.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Initialise une nouvelle instance de cette classe.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Remarques

Crée un nouveau[`DocumentBuilder`](../)objet et l'attache à un nouveau[`Document`](../../document/) objet. Des options de création de documents supplémentaires peuvent être spécifiées.

## Exemples

Montre comment ignorer la mise en forme du tableau pour le contenu après.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Ajoute du contenu avant le tableau.
// La taille de police par défaut est 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Modifie la taille de la police à l'intérieur du tableau.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Si ContextTableFormatting est vrai, la mise en forme du tableau n'est pas appliquée au contenu après.
// Si ContextTableFormatting est faux, la mise en forme du tableau est appliquée au contenu après.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Voir également

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Initialise une nouvelle instance de cette classe.

```csharp
public DocumentBuilder(Document doc)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | Document | Le[`Document`](../../document/) objet auquel s'attacher. |

## Remarques

Crée un nouveau[`DocumentBuilder`](../) objet, s'attache à l'objet spécifié[`Document`](../../document/) objet. Le curseur est positionné au début du document.

## Exemples

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez que nous voulons des en-têtes et des pieds de page différents pour les premières pages, les pages paires et les pages impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Créez les en-têtes, puis ajoutez trois pages au document pour afficher chaque type d'en-tête.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Montre comment insérer une table des matières (TOC) dans un document en utilisant des styles de titre comme entrées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une table des matières pour la première page du document.
// Configurez le tableau pour récupérer les paragraphes avec des titres de niveaux 1 à 3.
// Définissez également ses entrées comme des hyperliens qui nous mèneront
// à l'emplacement de l'en-tête lors d'un clic gauche dans Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Remplissez la table des matières en ajoutant des paragraphes avec des styles de titre.
// Chaque titre de ce type avec un niveau compris entre 1 et 3 créera une entrée dans le tableau.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Une table des matières est un champ d'un type qui doit être mis à jour pour afficher un résultat à jour.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Voir également

* class [Document](../../document/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Initialise une nouvelle instance de cette classe.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | Document | Le[`Document`](../../document/) objet auquel s'attacher. |
| options | DocumentBuilderOptions | Options supplémentaires pour le processus de création de documents. |

## Remarques

Crée un nouveau[`DocumentBuilder`](../) objet, s'attache à l'objet spécifié[`Document`](../../document/) objet. Le curseur est positionné au début du document.

## Exemples

Montre comment ignorer la mise en forme du tableau pour le contenu après.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Ajoute du contenu avant le tableau.
// La taille de police par défaut est 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Modifie la taille de la police à l'intérieur du tableau.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Si ContextTableFormatting est vrai, la mise en forme du tableau n'est pas appliquée au contenu après.
// Si ContextTableFormatting est faux, la mise en forme du tableau est appliquée au contenu après.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Voir également

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
