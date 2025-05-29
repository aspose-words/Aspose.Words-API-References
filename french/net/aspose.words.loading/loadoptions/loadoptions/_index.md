---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur LoadOptions, conçu pour initialiser sans effort une nouvelle instance avec des valeurs par défaut pour des performances et une efficacité optimales.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public LoadOptions()
```

## Exemples

Montre comment ouvrir un document HTML avec des images d'un flux à l'aide d'un URI de base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Transmettez l'URI du dossier de base lors de son chargement
    // afin que toutes les images avec des URI relatives dans le document HTML puissent être trouvées.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Vérifiez que la première forme du document contient une image valide.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié pour charger un document crypté.

```csharp
public LoadOptions(string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| password | String | Le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. |

## Exemples

Montre comment charger un document Microsoft Word chiffré.

```csharp
Document doc;

// Aspose.Words lève une exception si nous essayons d'ouvrir un document crypté sans son mot de passe.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Lors du chargement d'un tel document, le mot de passe est transmis au constructeur du document à l'aide d'un objet LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Il existe deux manières de charger un document chiffré avec un objet LoadOptions.
// 1 - Charger le document à partir du système de fichiers local par nom de fichier :
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Charger le document à partir d'un flux :
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Un raccourci pour initialiser une nouvelle instance de cette classe avec des propriétés définies sur les valeurs spécifiées.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| loadFormat | LoadFormat | Le format du document à charger. |
| password | String | Le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. |
| baseUri | String | La chaîne utilisée pour convertir les URI relatifs en URI absolus. Peut être`nul` ou chaîne vide. |

## Exemples

Montre comment enregistrer une page Web sous forme de fichier .docx.

```csharp
const string url = "https://produits.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // L'URL est à nouveau utilisée comme baseUri pour garantir que tous les chemins d'image relatifs sont récupérés correctement.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Chargez le document HTML à partir du flux et transmettez l'objet LoadOptions.
        Document doc = new Document(stream, options);

        // À ce stade, nous pouvons lire et modifier le contenu du document, puis l'enregistrer sur le système de fichiers local.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Montre comment spécifier un URI de base lors de l'ouverture d'un document HTML.

```csharp
// Supposons que nous voulions charger un document .html contenant une image liée par un URI relatif
// tant que l'image se trouve à un autre emplacement. Dans ce cas, nous devrons convertir l'URI relative en URI absolue.
 // Nous pouvons fournir un URI de base à l'aide d'un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Bien que l'image ait été cassée dans le fichier .html d'entrée, notre URI de base personnalisé nous a aidé à réparer le lien.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Ce document de sortie affichera l'image manquante.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Voir également

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
