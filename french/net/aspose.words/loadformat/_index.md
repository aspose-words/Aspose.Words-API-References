---
title: LoadFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Indique le format du document à charger.
type: docs
weight: 3350
url: /fr/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Indique le format du document à charger.

```csharp
public enum LoadFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `0` | Indique à Aspose.Words de reconnaître automatiquement le format. |
| Doc | `10` | Microsoft Word 95 ou Word 97 - Document 2003. |
| Dot | `11` | Microsoft Word 95 ou Word 97 - Modèle 2003. |
| DocPreWord60 | `12` | Le document est au format antérieur à Word 95. Aspose.Words ne prend actuellement pas en charge le chargement de tels documents. |
| Docx | `20` | Office Open XML WordprocessingML Document (sans macro). |
| Docm | `21` | Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | `22` | Modèle Office Open XML WordprocessingML (sans macro). |
| Dotm | `23` | Modèle compatible avec les macros Office Open XML WordprocessingML. |
| FlatOpc | `24` | Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Macro-Enabled Document stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplate | `26` | Modèle Office Open XML WordprocessingML (sans macro) stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML Macro-Enabled Template stocké dans un fichier XML plat au lieu d'un package ZIP. |
| Rtf | `30` | Format RTF. |
| WordML | `31` | Format Microsoft Word 2003 WordprocessingML. |
| Html | `50` | Format HTML. |
| Mhtml | `51` | Format MHTML (archive Web). |
| Mobi | `52` | format MOBI. Utilisé par le lecteur MobiPocket et les lecteurs Amazon Kindle. |
| Chm | `53` | format CHM (aide HTML compilée). |
| Azw3 | `54` | Format AZW3. Utilisé par les lecteurs Amazon Kindle. |
| Epub | `55` | Format EPUB. |
| Odt | `60` | Document texte ODF. |
| Ott | `61` | Modèle de document texte ODF. |
| Text | `62` | Texte brut. |
| Markdown | `63` | Document texte Markdown. |
| Pdf | `64` | Document PDF. |
| Xml | `65` | Document XML. |
| Unknown | `255` | Format non reconnu, ne peut pas être chargé par Aspose.Words. |

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

Montre comment utiliser les méthodes FileFormatUtil pour détecter le format d'un document.

```csharp
// Charge un document à partir d'un fichier auquel il manque une extension de fichier, puis détecte son format de fichier.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Vous trouverez ci-dessous deux méthodes de conversion d'un LoadFormat en son SaveFormat correspondant.
    // 1 - Récupère la chaîne d'extension de fichier pour le LoadFormat, puis récupère le SaveFormat correspondant à partir de cette chaîne :
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertit directement le LoadFormat en son SaveFormat :
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Chargez un document à partir du flux, puis enregistrez-le dans l'extension de fichier détectée automatiquement.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
