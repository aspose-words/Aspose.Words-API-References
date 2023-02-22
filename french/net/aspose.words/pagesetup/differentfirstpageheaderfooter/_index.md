---
title: PageSetup.DifferentFirstPageHeaderFooter
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Vrai si un entête ou un pied de page différent est utilisé sur la première page.
type: docs
weight: 110
url: /fr/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

**Vrai** si un en-tête ou un pied de page différent est utilisé sur la première page.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

### Exemples

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez que nous voulons des en-têtes et des pieds de page différents pour les premières pages, paires et impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crée les en-têtes, puis ajoute trois pages au document pour afficher chaque type d'en-tête.
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

Montre comment activer ou désactiver les en-têtes/pieds de page principaux.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'en-tête/pied de page.
// 1 - L'en-tête/pied de page "Premier", qui apparaît sur la première page de la section.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 - L'en-tête/pied de page "Primaire", qui apparaît sur chaque page de la section.
// Nous pouvons remplacer l'en-tête/pied de page principal par un premier et un en-tête/pied de page pair.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Chaque section a un objet "PageSetup" qui spécifie les propriétés liées à l'apparence de la page
// tels que l'orientation, la taille et les bordures.
// Définissez la propriété "DifferentFirstPageHeaderFooter" sur "true" pour appliquer le premier en-tête/pied de page à la première page.
// Définissez la propriété "DifferentFirstPageHeaderFooter" sur "false"
// pour que la première page affiche l'en-tête/le pied de page principal.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

Montre comment suivre l'ordre dans lequel une opération de remplacement de texte traverse les nœuds.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // L'utilisation d'un en-tête/pied de page différent pour la première page affectera l'ordre de recherche.
            firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
            doc.Range.Replace(new Regex("(header|footer)"), "", options);

#if NET48 || NET5_0_OR_GREATER || JAVA
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
                    logger.Text.Replace("\r", ""));
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
                    logger.Text.Replace("\r", ""));
#elif __MOBILE__
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger.Text);
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger.Text);
#endif
        }

        /// <summary>
        /// Au cours d'une opération de recherche et de remplacement, enregistre le contenu de chaque nœud contenant du texte que l'opération "trouve",
        /// dans l'état dans lequel il se trouve avant le remplacement.
        /// Cela affichera l'ordre dans lequel l'opération de remplacement de texte traverse les nœuds.
        /// </summary>
        private class ReplaceLog : IReplacingCallback
        {
            public ReplaceAction Replacing(ReplacingArgs args)
            {
                mTextBuilder.AppendLine(args.MatchNode.GetText());
                return ReplaceAction.Skip;
            }

            internal string Text => mTextBuilder.ToString();

            private readonly StringBuilder mTextBuilder = new StringBuilder();
        }
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


