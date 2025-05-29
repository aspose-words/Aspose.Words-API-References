---
title: RtfLoadOptions Class
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.RtfLoadOptions pour améliorer le chargement des documents RTF avec des paramètres personnalisables pour une intégration transparente dans vos projets.
type: docs
weight: 4170
url: /fr/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Permet de spécifier des options supplémentaires lors du chargementRtf document dans un[`Document`](../../aspose.words/document/) objet.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article de documentation.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions/)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtient ou définit s'il faut convertir le métafichier(Wmf ouEmf ) images àPngformat d'image. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtient ou définit s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié à l'intérieur du document. Peut être`nul` La valeur par défaut est`nul` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permet de spécifier les paramètres de police du document. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Spécifie s'il faut ignorer les données OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Spécifie le format du document à charger. La valeur par défaut estAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut estWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Appelé lors du chargement d'un document et accepte des données sur la progression du chargement. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | Lorsqu'il est réglé sur`vrai` , essaiera de détecter les caractères UTF8, ils seront conservés lors de l'importation. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Spécifie s'il faut mettre à jour les champs avec le`sale` attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Obtient ou définit s'il faut utiliser la valeur LCID obtenue à partir du registre Windows pour déterminer les marges par défaut de la configuration de la page. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Appelé lors d'une opération de chargement, lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

## Exemples

Montre comment détecter les caractères UTF-8 lors du chargement d'un document RTF.

```csharp
// Créez un objet « RtfLoadOptions » pour modifier la façon dont nous chargeons un document RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Définissez la propriété « RecognizeUtf8Text » sur « false » pour supposer que le document utilise le jeu de caractères ISO 8859-1
// et charge chaque caractère du document.
// Définissez la propriété « RecognizeUtf8Text » sur « true » pour analyser tous les caractères de longueur variable pouvant apparaître dans le texte.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Voir également

* class [LoadOptions](../loadoptions/)
* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
