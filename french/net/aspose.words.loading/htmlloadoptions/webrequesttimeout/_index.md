---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words pour .NET
description: HtmlLoadOptions WebRequestTimeout propriété. Le nombre de millisecondes à attendre avant lexpiration de la requête Web. La valeur par défaut est 100 000 milliseconds 100 secondes en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Le nombre de millisecondes à attendre avant l'expiration de la requête Web. La valeur par défaut est 100 000 milliseconds (100 secondes).

```csharp
public int WebRequestTimeout { get; set; }
```

## Remarques

Le nombre de millisecondes pendant lesquelles Aspose.Words attend une réponse lors du chargement de ressources externes (images, feuilles style ) liées dans des documents HTML et MHTML.

## Exemples

Montre comment définir une limite de temps pour les requêtes Web lors du chargement d'un document avec des ressources externes liées par des URL.

```csharp
public void WebRequestTimeout()
{
    // Créez un nouvel objet HtmlLoadOptions et vérifiez son seuil d'expiration pour une requête Web.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Lors du chargement d'un document Html avec des ressources liées en externe par une URL d'adresse web,
    // Aspose.Words annulera les requêtes Web qui ne parviennent pas à récupérer les ressources dans ce délai, en millisecondes.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Définit un WarningCallback qui enregistrera tous les avertissements qui se produisent pendant le chargement.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Charge un tel document et vérifie qu'une forme avec des données d'image a été créée.
    // Le chargement de cette image liée nécessitera le chargement d'une requête Web, qui devra être complétée dans notre délai.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Définissez un délai d'expiration déraisonnable et essayez à nouveau de charger le document.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Une requête Web qui ne parvient pas à obtenir une image dans le délai imparti produira quand même une image.
    // Cependant, l'image sera le « x » rouge qui signifie généralement des images manquantes.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Nous pouvons également configurer un rappel personnalisé pour récupérer les avertissements des requêtes Web expirées.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Stocke tous les avertissements qui se produisent lors d'une opération de chargement de document dans une liste.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
