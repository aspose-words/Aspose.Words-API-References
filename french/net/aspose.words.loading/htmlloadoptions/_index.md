---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Loading.HtmlLoadOptions pour améliorer le chargement de documents HTML dans un objet Document avec des options personnalisables pour des performances optimales.
type: docs
weight: 4070
url: /fr/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Permet de spécifier des options supplémentaires lors du chargement d'un document HTML dans un[`Document`](../../aspose.words/document/) objet.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article de documentation.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié pour charger un document crypté. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | Un raccourci pour initialiser une nouvelle instance de cette classe avec des propriétés définies sur les valeurs spécifiées. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Obtient ou définit une valeur qui spécifie comment les propriétés des éléments de niveau bloc sont importées. La valeur par défaut estMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtient ou définit s'il faut convertir le métafichier(Wmf ouEmf ) images àPngformat d'image. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtient ou définit s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut convertir les images SVG chargées au format EMF. La valeur par défaut est`FAUX` et, si possible, les images SVG chargées sont stockées telles quelles sans conversion. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié à l'intérieur du document. Peut être`nul` La valeur par défaut est`nul` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permet de spécifier les paramètres de police du document. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut ignorer les éléments HTML &lt;noscript&gt;. La valeur par défaut est`FAUX` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Spécifie s'il faut ignorer les données OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Spécifie le format du document à charger. La valeur par défaut estAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut estWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Obtient ou définit le type préféré de nœuds de document qui représenteront les éléments &lt;input&gt; et &lt;select&gt; importés. La valeur par défaut estFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Appelé lors du chargement d'un document et accepte des données sur la progression du chargement. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut prendre en charge les règles @font-face et s'il faut charger les polices déclarées. La valeur par défaut est`FAUX` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut prendre en charge les images VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Spécifie s'il faut mettre à jour les champs avec le`sale` attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Obtient ou définit s'il faut utiliser la valeur LCID obtenue à partir du registre Windows pour déterminer les marges par défaut de la configuration de la page. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Appelé lors d'une opération de chargement, lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité des données ou du formatage. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Le délai d'attente (en millisecondes) avant l'expiration de la requête web. La valeur par défaut est 100 000 millisecondes (100 secondes). |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

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

* class [LoadOptions](../loadoptions/)
* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
