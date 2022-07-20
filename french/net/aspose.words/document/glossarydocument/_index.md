---
title: GlossaryDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit le document de glossaire dans ce document ou modèle. Un document de glossaire est un stockage pour les entrées dinsertion automatique de correction automatique et de bloc de construction définies dans un document.
type: docs
weight: 170
url: /fr/net/aspose.words/document/glossarydocument/
---
## Document.GlossaryDocument property

Obtient ou définit le document de glossaire dans ce document ou modèle. Un document de glossaire est un stockage pour les entrées d'insertion automatique, de correction automatique et de bloc de construction définies dans un document.

```csharp
public GlossaryDocument GlossaryDocument { get; set; }
```

### Remarques

Cette propriété renvoie`nul` si le document n'a pas de document de glossaire.

Vous pouvez ajouter un document de glossaire à un document en créant a [`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument) objet et affectation à cette propriété.

### Exemples

Montre comment ajouter un bloc de construction personnalisé à un document.

```csharp
public void CreateAndInsert()
{
    // Le document glossaire d'un document stocke les blocs de construction.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Crée un bloc de construction, nomme-le, puis ajoute-le au document de glossaire.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Tous les nouveaux GUID de bloc de construction ont la même valeur zéro par défaut, et nous pouvons leur donner une nouvelle valeur unique.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Les propriétés suivantes catégorisent les blocs de construction
    // dans le menu auquel nous pouvons accéder dans Microsoft Word via "Insérer" -> "Parties rapides" -> "Organisateur de blocs de construction".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Avant de pouvoir ajouter ce bloc de construction à notre document, nous devrons lui donner un contenu,
    // que nous ferons en utilisant un visiteur de document. Ce visiteur définira également une catégorie, une galerie et un comportement.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Nous pouvons accéder au bloc que nous venons de créer à partir du document glossaire.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Le bloc lui-même est une section qui contient le texte.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Maintenant, nous pouvons l'insérer dans le document en tant que nouvelle section.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Nous pouvons également le trouver dans l'organisateur de blocs de construction de Microsoft Word et le placer manuellement.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Configure un bloc de construction visité à insérer dans le document en tant que partie rapide et ajoute du texte à son contenu.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Configurez le bloc de construction en tant que partie rapide et ajoutez les propriétés utilisées par Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Ajoute une section avec du texte.
        // L'insertion du bloc dans le document ajoutera cette section avec ses nœuds enfants à l'emplacement.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Voir également

* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument)
* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
