---
title: HtmlLoadOptions.HtmlLoadOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlLoadOptions constructeur. Initialise une nouvelle instance de cette classe avec les valeurs par défaut.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public HtmlLoadOptions()
```

### Exemples

Montre comment prendre en charge les commentaires conditionnels lors du chargement d'un document HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si la valeur est true, alors nous prenons en compte le code VML lors de l'analyse du document chargé.
loadOptions.SupportVml = supportVml;

// Ce document contient une image JPEG dans "<!--[if gte vml 1]>" Mots clés,
// et une image PNG différente dans "<![if !vml]>" Mots clés.
// Si nous définissons le drapeau "SupportVml" sur "true", alors Aspose.Words chargera le JPEG.
// Si nous définissons cet indicateur sur "false", alors Aspose.Words ne chargera que le PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../htmlloadoptions/)
* Assemblée [Aspose.Words](../../../)

---

## HtmlLoadOptions(string) {#constructor_2}

Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié pour charger un document chiffré.

```csharp
public HtmlLoadOptions(string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| password | String | Le mot de passe pour ouvrir un document crypté. Peut être une chaîne nulle ou vide. |

### Exemples

Montre comment chiffrer un document HTML, puis l'ouvrir à l'aide d'un mot de passe.

```csharp
// Crée et signe un document HTML chiffré à partir d'un .docx chiffré.
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

// Pour charger et lire ce document, nous aurons besoin de passer son déchiffrement
// mot de passe à l'aide d'un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../htmlloadoptions/)
* Assemblée [Aspose.Words](../../../)

---

## HtmlLoadOptions(LoadFormat, string, string) {#constructor_1}

Un raccourci pour initialiser une nouvelle instance de cette classe avec des propriétés définies sur les valeurs spécifiées.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| loadFormat | LoadFormat | Format du document à charger. |
| password | String | Le mot de passe pour ouvrir un document crypté. Peut être une chaîne nulle ou vide. |
| baseUri | String | La chaîne qui sera utilisée pour résoudre les URI relatifs en absolus. Peut être une chaîne nulle ou vide. |

### Exemples

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
* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../htmlloadoptions/)
* Assemblée [Aspose.Words](../../../)


