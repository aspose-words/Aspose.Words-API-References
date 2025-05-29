---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: Aspose.Words pour .NET
description: Découvrez la méthode LinkToPrevious dans HeaderFooterCollection pour connecter ou déconnecter facilement les en-têtes et les pieds de page dans les sections de votre document pour une mise en forme transparente.
type: docs
weight: 20
url: /fr/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

Lie ou dissocie tous les en-têtes et pieds de page aux en-têtes et pieds de page correspondants dans la section précédente.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `vrai` pour lier les en-têtes et les pieds de page à la section précédente ; `FAUX` pour les dissocier. |

## Remarques

Si l'un des en-têtes ou pieds de page n'existe pas, il les crée automatiquement.

## Exemples

Montre comment lier les en-têtes et les pieds de page entre les sections.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Accédez à la première section et créez un en-tête et un pied de page. Par défaut,
// l'en-tête et le pied de page n'apparaîtront que sur les pages de la section qui les contient.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Nous pouvons lier les en-têtes/pieds de page d'une section aux en-têtes/pieds de page de la section précédente
// pour permettre à la section de liaison d'afficher les en-têtes/pieds de page de la section liée.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Chaque section conservera ses propres objets d'en-tête et de pied de page. Lorsque nous lions des sections,
// la section de liaison affichera l'en-tête/les pieds de page de la section liée tout en conservant les siens.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Liez les en-têtes/pieds de page de la troisième section aux en-têtes/pieds de page de la deuxième section.
// La deuxième section est déjà liée à l'en-tête/pied de page de la première section,
// donc le lien vers la deuxième section créera une chaîne de liens.
// Les première, deuxième et maintenant troisième sections afficheront toutes les en-têtes de la première section.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Nous pouvons dissocier l'en-tête/les pieds de page d'une section précédente en passant « false » lors de l'appel de la méthode LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Nous pouvons également sélectionner uniquement un type spécifique d'en-tête/pied de page à lier à l'aide de cette méthode.
// La troisième section aura désormais le même pied de page que les deuxième et première sections, mais pas l'en-tête.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// L'en-tête/les pieds de page de la première section ne peuvent pas se lier à quoi que ce soit car il n'y a pas de section précédente.
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

* class [HeaderFooterCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## LinkToPrevious(*[HeaderFooterType](../../headerfootertype/), bool*) {#linktoprevious}

Lie ou dissocie l'en-tête ou le pied de page spécifié de l'en-tête ou du pied de page correspondant dans la section précédente.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | UN[`HeaderFooterType`](../../headerfootertype/) value qui spécifie l'en-tête ou le pied de page à lier/dissocier. |
| isLinkToPrevious | Boolean | `vrai` pour lier l'en-tête ou le pied de page à la section précédente ; `FAUX` pour dissocier. |

## Remarques

Si l'en-tête ou le pied de page du type spécifié n'existe pas, il est créé automatiquement.

## Exemples

Montre comment lier les en-têtes et les pieds de page entre les sections.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Accédez à la première section et créez un en-tête et un pied de page. Par défaut,
// l'en-tête et le pied de page n'apparaîtront que sur les pages de la section qui les contient.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Nous pouvons lier les en-têtes/pieds de page d'une section aux en-têtes/pieds de page de la section précédente
// pour permettre à la section de liaison d'afficher les en-têtes/pieds de page de la section liée.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Chaque section conservera ses propres objets d'en-tête et de pied de page. Lorsque nous lions des sections,
// la section de liaison affichera l'en-tête/les pieds de page de la section liée tout en conservant les siens.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Liez les en-têtes/pieds de page de la troisième section aux en-têtes/pieds de page de la deuxième section.
// La deuxième section est déjà liée à l'en-tête/pied de page de la première section,
// donc le lien vers la deuxième section créera une chaîne de liens.
// Les première, deuxième et maintenant troisième sections afficheront toutes les en-têtes de la première section.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Nous pouvons dissocier l'en-tête/les pieds de page d'une section précédente en passant « false » lors de l'appel de la méthode LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Nous pouvons également sélectionner uniquement un type spécifique d'en-tête/pied de page à lier à l'aide de cette méthode.
// La troisième section aura désormais le même pied de page que les deuxième et première sections, mais pas l'en-tête.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// L'en-tête/les pieds de page de la première section ne peuvent pas se lier à quoi que ce soit car il n'y a pas de section précédente.
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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
