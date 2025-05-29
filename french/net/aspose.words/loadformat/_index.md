---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.LoadFormat, définissant des formats de documents pour un chargement transparent et une compatibilité améliorée dans vos applications.
type: docs
weight: 4000
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
| Auto | `0` | Demande à Aspose.Words de reconnaître automatiquement le format. |
| MsWorks | `8` | Document Microsoft Works 8. |
| Doc | `10` | Document Microsoft Word 95 ou Word 97 - 2003. |
| Dot | `11` | Modèle Microsoft Word 95 ou Word 97 - 2003. |
| DocPreWord60 | `12` | Le document est au format antérieur à Word 95. Aspose.Words ne prend actuellement pas en charge le chargement de tels documents. |
| Docx | `20` | Document WordprocessingML Office Open XML (sans macro). |
| Docm | `21` | Document Office Open XML WordprocessingML prenant en charge les macros. |
| Dotx | `22` | Modèle WordprocessingML Office Open XML (sans macro). |
| Dotm | `23` | Modèle Office Open XML WordprocessingML avec macros activées. |
| FlatOpc | `24` | Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Document activé par macro stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplate | `26` | Modèle WordprocessingML Office Open XML (sans macro) stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Modèle Office Open XML WordprocessingML avec macros stockées dans un fichier XML plat au lieu d'un package ZIP. |
| Rtf | `30` | Format RTF. |
| WordML | `31` | Microsoft Word 2003 Format WordprocessingML. |
| Html | `50` | Format HTML. |
| Mhtml | `51` | Format MHTML (archive Web). |
| Mobi | `52` | Format MOBI. Utilisé par les lecteurs MobiPocket et Amazon Kindle. |
| Chm | `53` | Format CHM (Aide HTML compilée). |
| Azw3 | `54` | Format AZW3. Utilisé par les liseuses Amazon Kindle. |
| Epub | `55` | Format EPUB. |
| Odt | `60` | Document texte ODF. |
| Ott | `61` | Modèle de document texte ODF. |
| Text | `62` | Texte brut. |
| Markdown | `63` | Document texte Markdown. |
| Pdf | `64` | Document PDF. |
| Xml | `65` | Document XML. |
| Unknown | `255` | Format non reconnu, ne peut pas être chargé par Aspose.Words. |

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

Montre comment utiliser les méthodes FileFormatUtil pour détecter le format d'un document.

```csharp
// Chargez un document à partir d'un fichier auquel il manque une extension de fichier, puis détectez son format de fichier.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Vous trouverez ci-dessous deux méthodes de conversion d'un LoadFormat en son SaveFormat correspondant.
    // 1 - Récupérez la chaîne d'extension de fichier pour le LoadFormat, puis récupérez le SaveFormat correspondant à partir de cette chaîne :
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertissez le LoadFormat directement en son SaveFormat :
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
