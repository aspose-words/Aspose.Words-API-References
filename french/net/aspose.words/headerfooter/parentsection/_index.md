---
title: HeaderFooter.ParentSection
second_title: Référence de l'API Aspose.Words pour .NET
description: HeaderFooter propriété. Obtient la section parent de cette histoire.
type: docs
weight: 60
url: /fr/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

Obtient la section parent de cette histoire.

```csharp
public Section ParentSection { get; }
```

### Remarques

`ParentSection` est équivalent à[`ParentNode`](../../node/parentnode/) jeté à[`Section`](../../section/).

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

* class [Section](../../section/)
* class [HeaderFooter](../)
* espace de noms [Aspose.Words](../../headerfooter/)
* Assemblée [Aspose.Words](../../../)


