---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur HtmlLoadOptions, conçu pour initialiser sans effort des instances avec des paramètres par défaut pour un développement Web transparent.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public HtmlLoadOptions()
```

## Exemples

Montre comment prendre en charge les commentaires conditionnels lors du chargement d'un document HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si la valeur est vraie, nous prenons en compte le code VML lors de l'analyse du document chargé.
loadOptions.SupportVml = supportVml;

// Ce document contient une image JPEG dans les balises « <!--[if gte vml 1]> »,
// et une image PNG différente dans les balises "<![if !vml]>".
// Si nous définissons l'indicateur « SupportVml » sur « true », alors Aspose.Words chargera le JPEG.
// Si nous définissons cet indicateur sur « false », alors Aspose.Words chargera uniquement le PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)

---

## HtmlLoadOptions(*string*) {#constructor_2}

Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié pour charger un document crypté.

```csharp
public HtmlLoadOptions(string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| password | String | Le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. |

## Exemples

Montre comment crypter un document HTML, puis l'ouvrir à l'aide d'un mot de passe.

```csharp
// Créez et signez un document HTML chiffré à partir d'un fichier .docx chiffré.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Pour charger et lire ce document, nous devrons passer son décryptage
// mot de passe à l'aide d'un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)

---

## HtmlLoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Un raccourci pour initialiser une nouvelle instance de cette classe avec des propriétés définies sur les valeurs spécifiées.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| loadFormat | LoadFormat | Le format du document à charger. |
| password | String | Le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. |
| baseUri | String | La chaîne utilisée pour convertir les URI relatifs en URI absolus. Peut être`nul` ou chaîne vide. |

## Exemples

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
* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
