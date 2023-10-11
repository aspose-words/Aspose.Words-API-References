---
title: CustomXmlProperty.CustomXmlProperty
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomXmlProperty constructeur. Initialise une nouvelle instance de cette classe.
type: docs
weight: 10
url: /fr/net/aspose.words.markup/customxmlproperty/customxmlproperty/
---
## CustomXmlProperty constructor

Initialise une nouvelle instance de cette classe.

```csharp
public CustomXmlProperty(string name, string uri, string value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. C'est pas possible`nul`. |
| uri | String | L’URI de l’espace de noms de la propriété. C'est pas possible`nul`. |
| value | String | La valeur de la propriété. C'est pas possible`nul`. |

### Exemples

Montre comment créer des balises intelligentes.

```csharp
public void Create()
{
    Document doc = new Document();

    // Une balise active apparaît dans un document avec Microsoft Word qui reconnaît une partie de son texte comme une forme de données,
    // tel qu'un nom, une date ou une adresse, et le convertit en un lien hypertexte affichant un soulignement en pointillés violets.
    SmartTag smartTag = new SmartTag(doc);

    // Les balises intelligentes sont des nœuds composites qui contiennent leur texte reconnu dans son intégralité.
    // Ajoutez manuellement du contenu à cette balise active.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word peut reconnaître le contenu ci-dessus comme étant une date.
    // Les balises intelligentes utilisent la propriété "Element" pour refléter le type de données qu'elles contiennent.
    smartTag.Element = "date";

    // Certains types de balises actives traitent davantage leur contenu dans des propriétés XML personnalisées.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Définit l'URI de la balise intelligente sur la valeur par défaut.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Créez une autre balise intelligente pour un téléscripteur boursier.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Imprime toutes les balises intelligentes de notre document à l'aide d'un visiteur de document.
    doc.Accept(new SmartTagPrinter());

    // Les anciennes versions de Microsoft Word prennent en charge les balises actives.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Utilisez la méthode "RemoveSmartTags" pour supprimer toutes les balises intelligentes d'un document.
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

* class [CustomXmlProperty](../)
* espace de noms [Aspose.Words.Markup](../../customxmlproperty/)
* Assemblée [Aspose.Words](../../../)


