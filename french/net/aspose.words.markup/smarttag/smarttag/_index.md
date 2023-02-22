---
title: SmartTag.SmartTag
second_title: Référence de l'API Aspose.Words pour .NET
description: SmartTag constructeur. Initialise une nouvelle instance duSmartTag classe.
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

### Remarques

Lorsque vous créez un nouveau nœud, vous devez spécifier un document auquel le nœud appartient. Un nœud ne peut pas exister sans document car il dépend des structures à l'échelle du document telles que les listes et les styles. Bien qu'un nœud appartienne toujours à un document, un nœud peut ou peut ne pas faire partie de l'arborescence du document.

Lorsqu'un nœud est créé, il appartient à un document, mais ne fait pas encore partie de l'arborescence du document et[`ParentNode`](../../../aspose.words/node/parentnode/) est nul. Pour insérer un nœud dans le document, utilisez the [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) ou[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) method sur le nœud parent.

### Exemples

Montre comment créer des balises actives.

```csharp
public void Create()
{
    Document doc = new Document();

    // Une balise active apparaît dans un document avec Microsoft Word reconnaît une partie de son texte comme une forme de données,
    // tel qu'un nom, une date ou une adresse, et le convertit en un lien hypertexte qui affiche un soulignement pointillé violet.
    SmartTag smartTag = new SmartTag(doc);

    // Les balises actives sont des nœuds composites qui contiennent leur texte reconnu dans son intégralité.
    // Ajouter manuellement du contenu à cette balise active.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word peut reconnaître le contenu ci-dessus comme étant une date.
    // Les balises actives utilisent la propriété "Element" pour refléter le type de données qu'elles contiennent.
    smartTag.Element = "date";

    // Certains types de balises actives traitent davantage leur contenu dans des propriétés XML personnalisées.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Définissez l'URI de la balise intelligente sur la valeur par défaut.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Crée une autre balise intelligente pour un symbole boursier.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Imprimer toutes les balises actives de notre document à l'aide d'un visiteur de document.
    doc.Accept(new SmartTagPrinter());

    // Les anciennes versions de Microsoft Word prennent en charge les balises actives.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Utilisez la méthode "RemoveSmartTags" pour supprimer toutes les balises actives d'un document.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Imprime les balises actives visitées et leur contenu.
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
* espace de noms [Aspose.Words.Markup](../../smarttag/)
* Assemblée [Aspose.Words](../../../)


