---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words pour .NET
description: Aspose.Words.LoadFormat énumération. Indique le format du document à charger en C#.
type: docs
weight: 3550
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
| Doc | `10` | Microsoft Word 95 ou Word 97 - Document 2003. |
| Dot | `11` | Modèle Microsoft Word 95 ou Word 97 - 2003. |
| DocPreWord60 | `12` | Le document est au format antérieur à Word 95. Aspose.Words ne prend actuellement pas en charge le chargement de tels documents. |
| Docx | `20` | Document Office Open XML WordprocessingML (sans macro). |
| Docm | `21` | Document Office Open XML WordprocessingML prenant en charge les macros. |
| Dotx | `22` | Modèle Office Open XML WordprocessingML (sans macro). |
| Dotm | `23` | Modèle Office Open XML WordprocessingML prenant en charge les macros. |
| FlatOpc | `24` | Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcMacroEnabled | `25` | Document Office Open XML WordprocessingML prenant en charge les macros stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplate | `26` | Modèle WordprocessingML Office Open XML (sans macro) stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Modèle Office Open XML WordprocessingML prenant en charge les macros stocké dans un fichier XML plat au lieu d'un package ZIP. |
| Rtf | `30` | Format RTF. |
| WordML | `31` | Format WordprocessingML Microsoft Word 2003. |
| Html | `50` | Format HTML. |
| Mhtml | `51` | Format MHTML (archive Web). |
| Mobi | `52` | Format MOBI. Utilisé par le lecteur MobiPocket et les lecteurs Amazon Kindle. |
| Chm | `53` | Format CHM (Aide HTML compilée). |
| Azw3 | `54` | Format AZW3. Utilisé par les lecteurs Amazon Kindle. |
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
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // L'URL est à nouveau utilisée comme baseUri pour garantir que tous les chemins d'image relatifs sont récupérés correctement.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Charge le document HTML depuis le flux et passe l'objet LoadOptions.
        Document doc = new Document(stream, options);

        // A ce stade, nous pouvons lire et modifier le contenu du document, puis l'enregistrer dans le système de fichiers local.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Montre comment spécifier un URI de base lors de l'ouverture d'un document HTML.

```csharp
// Supposons que nous voulions charger un document .html contenant une image liée par un URI relatif
// alors que l'image se trouve à un emplacement différent. Dans ce cas, nous devrons résoudre l’URI relatif en un URI absolu.
 // Nous pouvons fournir un URI de base en utilisant un objet HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Alors que l'image était cassée dans l'entrée .html, notre URI de base personnalisé nous a aidé à réparer le lien.
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

    // Vous trouverez ci-dessous deux méthodes pour convertir un LoadFormat en son SaveFormat correspondant.
    // 1 - Récupère la chaîne d'extension de fichier pour LoadFormat, puis récupère le SaveFormat correspondant à partir de cette chaîne :
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertir le LoadFormat directement en son SaveFormat :
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Charge un document à partir du flux, puis enregistre-le sous l'extension de fichier automatiquement détectée.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
