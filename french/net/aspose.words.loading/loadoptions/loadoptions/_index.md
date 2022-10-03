---
title: LoadOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Initialise une nouvelle instance de cette classe avec les valeurs par défaut.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public LoadOptions()
```

### Exemples

Montre comment ouvrir un document HTML avec des images d'un flux à l'aide d'un URI de base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passer l'URI du dossier de base lors de son chargement
    // afin que toutes les images avec des URI relatifs dans le document HTML puissent être trouvées.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Vérifie que la première forme du document contient une image valide.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié pour charger un document chiffré.

```csharp
public LoadOptions(string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| password | String | Le mot de passe pour ouvrir un document crypté. Peut être une chaîne nulle ou vide. |

### Exemples

Montre comment charger un document Microsoft Word crypté.

```csharp
Document doc;

// Aspose.Words lance une exception si nous essayons d'ouvrir un document chiffré sans son mot de passe.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Lors du chargement d'un tel document, le mot de passe est transmis au constructeur du document à l'aide d'un objet LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Il existe deux manières de charger un document chiffré avec un objet LoadOptions.
// 1 - Charger le document depuis le système de fichiers local par nom de fichier :
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Charger le document depuis un flux :
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

Un raccourci pour initialiser une nouvelle instance de cette classe avec des propriétés définies sur les valeurs spécifiées.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| loadFormat | LoadFormat | Format du document à charger. |
| password | String | Le mot de passe pour ouvrir un document crypté. Peut être une chaîne nulle ou vide. |
| baseUri | String | La chaîne qui sera utilisée pour résoudre les URI relatifs en absolus. Peut être une chaîne nulle ou vide. |

### Exemples

Montre comment enregistrer une page Web en tant que fichier .docx.

```csharp
const string url = "http://www.aspose.com/" ;

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // L'URL est à nouveau utilisée comme baseUri pour s'assurer que tous les chemins d'image relatifs sont récupérés correctement.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Charge le document HTML à partir du flux et transmet l'objet LoadOptions.
        Document doc = new Document(stream, options);

        // À ce stade, nous pouvons lire et modifier le contenu du document, puis l'enregistrer dans le système de fichiers local.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Montre comment spécifier un URI de base lors de l'ouverture d'un document html.

```csharp
// Supposons que nous voulions charger un document .html contenant une image liée par une URI relative
// alors que l'image est dans un endroit différent. Dans ce cas, nous devrons résoudre l'URI relatif en un absolu.
 // Nous pouvons fournir un URI de base en utilisant un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Alors que l'image était cassée dans l'entrée .html, notre URI de base personnalisé nous a aidés à réparer le lien.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Ce document de sortie affichera l'image manquante.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Voir également

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
