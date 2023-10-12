---
title: HeaderFooterCollection.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: HeaderFooterCollection propriété. Récupère unHeaderFooter à lindex donné.
type: docs
weight: 10
url: /fr/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Récupère un[`HeaderFooter`](../../headerfooter/) à l'index donné.

```csharp
public HeaderFooter this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index dans la collection. |

### Remarques

L'indice est de base zéro.

Les index négatifs sont autorisés et indiquent un accès depuis l'arrière de la collection. Par exemple -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments de la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments de la liste, cela renvoie une référence nulle.

### Exemples

Montre comment lier les en-têtes et les pieds de page entre les sections.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Passe à la première section et crée un en-tête et un pied de page. Par défaut,
// l'en-tête et le pied de page n'apparaîtront que sur les pages de la section qui les contient.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// On peut lier les en-têtes/pieds de page d'une section aux en-têtes/pieds de page de la section précédente
// pour permettre à la section de liaison d'afficher les en-têtes/pieds de page de la section liée.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Chaque section aura toujours ses propres objets d'en-tête/pied de page. Lorsque nous lions des sections,
// la section de liaison affichera l'en-tête/pied de page de la section liée tout en conservant les siens.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Liez les en-têtes/pieds de page de la troisième section aux en-têtes/pieds de page de la deuxième section.
// La deuxième section est déjà liée aux en-têtes/pieds de page de la première section,
// donc créer un lien vers la deuxième section créera une chaîne de liens.
// Les première, deuxième et maintenant troisième sections afficheront toutes les en-têtes de la première section.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Nous pouvons dissocier l'en-tête/pied de page d'une section précédente en passant "false" lors de l'appel de la méthode LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Nous pouvons également sélectionner uniquement un type spécifique d'en-tête/pied de page à lier en utilisant cette méthode.
// La troisième section aura désormais le même pied de page que les deuxième et première sections, mais pas l'en-tête.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// L'en-tête/pied de page de la première section ne peut pas se lier à quoi que ce soit car il n'y a pas de section précédente.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Tous les en-têtes/pieds de page de la deuxième section sont liés aux en-têtes/pieds de page de la première section.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Dans la troisième section, seul le pied de page est lié au pied de page de la première section via la deuxième section.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Voir également

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* espace de noms [Aspose.Words](../../headerfootercollection/)
* Assemblée [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Récupère un[`HeaderFooter`](../../headerfooter/) du type spécifié.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Paramètre | La description |
| --- | --- |
| headerFooterType | UN[`HeaderFooterType`](../../headerfootertype/) value qui spécifie le type d'en-tête/pied de page à récupérer. |

### Remarques

Retours`nul` si l'en-tête/pied de page du type spécifié est introuvable.

### Exemples

Montre comment remplacer du texte dans le pied de page d'un document.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Montre comment supprimer tous les pieds de page d’un document.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Parcourez chaque section et supprimez les pieds de page de toutes sortes.
foreach (Section section in doc.OfType<Section>())
{
    // Il existe trois types de types de pied de page et d'en-tête.
    // 1 - L'en-tête/pied de page "Premier", qui n'apparaît que sur la première page d'une section.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - L'en-tête/pied de page "Primaire", qui apparaît sur les pages impaires.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - L'en-tête/pied de page "Pair", qui apparaît sur les pages paires.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Voir également

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* espace de noms [Aspose.Words](../../headerfootercollection/)
* Assemblée [Aspose.Words](../../../)


