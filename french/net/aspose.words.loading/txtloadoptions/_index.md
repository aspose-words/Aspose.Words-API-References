---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.TxtLoadOptions pour un chargement optimisé des documents texte. Personnalisez votre objet Document avec des options flexibles pour des performances optimales.
type: docs
weight: 4190
url: /fr/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Permet de spécifier des options supplémentaires lors du chargementText document dans un[`Document`](../../aspose.words/document/) objet.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article de documentation.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Obtient ou définit une valeur booléenne indiquant que la détection de numérotation automatique sera effectuée lors du chargement d'un document. La valeur par défaut est`vrai` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtient ou définit s'il faut convertir le métafichier(Wmf ouEmf ) images àPngformat d'image. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtient ou définit s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | Spécifie soit de détecter les hyperliens dans le texte. La valeur par défaut est`FAUX` . |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Permet de spécifier comment les éléments de liste numérotés sont reconnus lorsque le document est importé à partir d'un format texte brut. La valeur par défaut est`vrai`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Obtient ou définit une direction de document. La valeur par défaut estLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié à l'intérieur du document. Peut être`nul` La valeur par défaut est`nul` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permet de spécifier les paramètres de police du document. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Spécifie s'il faut ignorer les données OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Obtient ou définit l'option préférée d'une gestion d'espace de début. La valeur par défaut estConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Spécifie le format du document à charger. La valeur par défaut estAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut estWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Appelé lors du chargement d'un document et accepte des données sur la progression du chargement. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Obtient ou définit l'option préférée d'une gestion d'espace de fin. La valeur par défaut estTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Spécifie s'il faut mettre à jour les champs avec le`sale` attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Obtient ou définit s'il faut utiliser la valeur LCID obtenue à partir du registre Windows pour déterminer les marges par défaut de la configuration de la page. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Appelé lors d'une opération de chargement, lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

## Exemples

Montre comment lire et afficher les hyperliens.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Charger le document avec des hyperliens.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Imprimer le texte des hyperliens.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Voir également

* class [LoadOptions](../loadoptions/)
* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
