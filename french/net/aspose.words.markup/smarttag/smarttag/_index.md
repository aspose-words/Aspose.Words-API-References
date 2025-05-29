---
title: SmartTag
linktitle: SmartTag
articleTitle: SmartTag
second_title: Aspose.Words pour .NET
description: Créez facilement des SmartTags dynamiques grâce à notre outil de création. Optimisez vos projets grâce à des fonctionnalités personnalisables et une intégration fluide pour des performances optimales.
type: docs
weight: 10
url: /fr/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Initialise une nouvelle instance du[`SmartTag`](../) classe.

```csharp
public SmartTag(DocumentBase doc)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |

## Remarques

Lors de la création d'un nœud, vous devez spécifier le document auquel il appartient. Un nœud ne peut exister sans document, car il dépend des structures du document, telles que les listes et les styles. Bien qu'un nœud appartienne toujours à un document, il peut faire partie de l'arborescence du document ou non.

Lorsqu'un nœud est créé, il appartient à un document, mais ne fait pas encore partie de l'arborescence du document et[`ParentNode`](../../../aspose.words/node/parentnode/) est nul. Pour insérer un nœud dans le document, utilisez the [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) ou[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)méthodes sur le nœud parent.

## Exemples

Montre comment créer des balises intelligentes.

```csharp
public void Create()
{
    Document doc = new Document();

    // Une balise active apparaît dans un document avec Microsoft Word qui reconnaît une partie de son texte comme une forme de données,
    // comme un nom, une date ou une adresse, et le convertit en un lien hypertexte qui affiche un soulignement en pointillé violet.
    SmartTag smartTag = new SmartTag(doc);

    // Les balises intelligentes sont des nœuds composites qui contiennent leur texte reconnu dans son intégralité.
    // Ajoutez manuellement du contenu à cette balise intelligente.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word peut reconnaître le contenu ci-dessus comme étant une date.
    // Les balises intelligentes utilisent la propriété « Élément » pour refléter le type de données qu'elles contiennent.
    smartTag.Element = "date";

    // Certains types de balises intelligentes traitent ensuite leur contenu dans des propriétés XML personnalisées.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Définissez l'URI de la balise intelligente sur la valeur par défaut.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Créez une autre balise intelligente pour un symbole boursier.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Imprimez toutes les balises intelligentes de notre document à l'aide d'un visiteur de document.
    doc.Accept(new SmartTagPrinter());

    // Les anciennes versions de Microsoft Word prennent en charge les balises intelligentes.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Utilisez la méthode « RemoveSmartTags » pour supprimer toutes les balises intelligentes d'un document.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Imprime les balises intelligentes visitées et leur contenu.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Appelé lorsqu'un nœud SmartTag est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsque la visite d'un nœud SmartTag est terminée.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Voir également

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
