---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Accept de BuildingBlock pour interagir facilement avec vos visiteurs et améliorer leur expérience. Libérez tout le potentiel de votre site web dès aujourd'hui !
type: docs
weight: 130
url: /fr/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; faux si[`DocumentVisitor`](../../../aspose.words/documentvisitor/) a arrêté l'opération avant de visiter tous les nœuds.

## Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

Appels[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) , puis appelle [`Accept`](../../../aspose.words/node/accept/) pour tous les nœuds enfants de ce bloc de construction, puis appelle [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Remarque : un nœud de bloc de construction et ses enfants ne sont pas visités lorsque vous exécutez un visiteur sur un[`Document`](../../../aspose.words/document/) . Si vous souhaitez exécuter un visiteur sur un bloc de construction a , vous devez exécuter le visiteur sur[`GlossaryDocument`](../../glossarydocument/) appel or `Accept` .

## Exemples

Montre comment ajouter un bloc de construction personnalisé à un document.

```csharp
public void CreateAndInsert()
{
    // Le glossaire d'un document stocke les blocs de construction.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Créez un bloc de construction, nommez-le, puis ajoutez-le au document de glossaire.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Tous les nouveaux GUID de blocs de construction ont la même valeur zéro par défaut, et nous pouvons leur donner une nouvelle valeur unique.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Les propriétés suivantes catégorisent les blocs de construction
    // dans le menu auquel nous pouvons accéder dans Microsoft Word via "Insertion" -> "Parties rapides" -> "Organisateur de blocs de construction".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Avant de pouvoir ajouter ce bloc de construction à notre document, nous devrons lui donner du contenu,
    // que nous réaliserons à l'aide d'un visiteur de document. Ce visiteur définira également une catégorie, une galerie et un comportement.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Visitez le début/la fin du BuildingBlock.
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

        // Ajouter une section avec du texte.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* espace de noms [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* Assemblée [Aspose.Words](../../../)
