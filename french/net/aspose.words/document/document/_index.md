---
title: Document
second_title: Référence de l'API Aspose.Words pour .NET
description: Crée un document Word vierge.
type: docs
weight: 10
url: /fr/net/aspose.words/document/document/
---
## Document() {#constructor}

Crée un document Word vierge.

```csharp
public Document()
```

### Remarques

Le format de papier du document est Letter par défaut. Si vous souhaitez modifier la configuration de la page, use [`Section.PageSetup`](../../section/pagesetup/).

Après la création, vous pouvez utiliser[`DocumentBuilder`](../../documentbuilder/) pour ajouter facilement du contenu au document.

### Exemples

Montre comment formater une suite de texte à l'aide de sa propriété de police.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Montre comment créer et charger des documents.

```csharp
// Il existe deux façons de créer un objet Document en utilisant Aspose.Words.
// 1 - Créer un document vierge :
Document doc = new Document();

// Les nouveaux objets Document sont livrés par défaut avec l'ensemble minimal de nœuds
// requis pour commencer à ajouter du contenu tel que du texte et des formes : une section, un corps et un paragraphe.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Chargez un document existant dans le système de fichiers local :
doc = new Document(MyDir + "Document.docx");

// Les documents chargés auront un contenu auquel nous pourrons accéder et modifier.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Certaines opérations qui doivent se produire lors du chargement, telles que l'utilisation d'un mot de passe pour déchiffrer un document,
// peut être fait en passant un objet LoadOptions lors du chargement du document.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Document(string) {#constructor_3}

Ouvre un document existant à partir d'un fichier. Détecte automatiquement le format de fichier.

```csharp
public Document(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom de fichier du document à ouvrir. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentException | Le nom du fichier ne peut pas être nul ou une chaîne vide. |

### Exemples

Montre comment ouvrir un document et le convertir en .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Montre comment convertir un PDF en .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Chargez le document PDF que nous venons d'enregistrer et convertissez-le en .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Montre comment charger un PDF.

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Vous trouverez ci-dessous deux manières de charger des documents PDF à l'aide des produits Aspose.
// 1 - Charger en tant que document Aspose.Words :
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Charger en tant que document Aspose.Pdf :
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Document(string, LoadOptions) {#constructor_4}

Ouvre un document existant à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom de fichier du document à ouvrir. |
| loadOptions | LoadOptions | Options supplémentaires à utiliser lors du chargement d'un document. Peut être nul. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentException | Le nom du fichier ne peut pas être nul ou une chaîne vide. |

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

Montre comment créer et charger des documents.

```csharp
// Il existe deux façons de créer un objet Document en utilisant Aspose.Words.
// 1 - Créer un document vierge :
Document doc = new Document();

// Les nouveaux objets Document sont livrés par défaut avec l'ensemble minimal de nœuds
// requis pour commencer à ajouter du contenu tel que du texte et des formes : une section, un corps et un paragraphe.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Chargez un document existant dans le système de fichiers local :
doc = new Document(MyDir + "Document.docx");

// Les documents chargés auront un contenu auquel nous pourrons accéder et modifier.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Certaines opérations qui doivent se produire lors du chargement, telles que l'utilisation d'un mot de passe pour déchiffrer un document,
// peut être fait en passant un objet LoadOptions lors du chargement du document.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Document(Stream) {#constructor_1}

Ouvre un document existant à partir d'un flux. Détecte automatiquement le format de fichier.

```csharp
public Document(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Flux à partir duquel charger le document. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentNullException | Le flux ne peut pas être nul. |
| NotSupportedException | Le flux ne prend pas en charge la lecture ou la recherche. |
| ObjectDisposedException | Le flux est un objet disposé. |

### Remarques

Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

### Exemples

Montre comment charger un document à l'aide d'un flux.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Montre comment charger un document à partir d'une URL.

```csharp
// Crée une URL qui pointe vers un document Microsoft Word.
const string url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx" ;

// Téléchargez le document dans un tableau d'octets, puis chargez ce tableau dans un document à l'aide d'un flux de mémoire.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // À ce stade, nous pouvons lire et modifier le contenu du document, puis l'enregistrer dans le système de fichiers local.
        Assert.AreEqual("Use this section to highlight your relevant passions, activities, and how you like to give back. " +
                        "It’s good to include Leadership and volunteer experiences here. " +
                        "Or show off important extras like publications, certifications, languages and more.",
            doc.FirstSection.Body.Paragraphs[4].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Document(Stream, LoadOptions) {#constructor_2}

Ouvre un document existant à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux à partir duquel charger le document. |
| loadOptions | LoadOptions | Options supplémentaires à utiliser lors du chargement d'un document. Peut être nul. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Le format du document n'est pas reconnu ou n'est pas pris en charge. |
| [FileCorruptedException](../../filecorruptedexception/) | Le document semble être corrompu et ne peut pas être chargé. |
| Exception | Il y a un problème avec le document et il doit être signalé aux développeurs Aspose.Words. |
| IOException | Il y a une exception d'entrée/sortie. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Le document est crypté et nécessite un mot de passe pour s'ouvrir, mais vous avez fourni un mot de passe incorrect. |
| ArgumentNullException | Le flux ne peut pas être nul. |
| NotSupportedException | Le flux ne prend pas en charge la lecture ou la recherche. |
| ObjectDisposedException | Le flux est un objet disposé. |

### Remarques

Le document doit être stocké au début du flux. Le flux doit prendre en charge le positionnement aléatoire.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
