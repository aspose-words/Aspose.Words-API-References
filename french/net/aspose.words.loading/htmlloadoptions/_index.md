---
title: HtmlLoadOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Permet de spécifier des options supplémentaires lors du chargement dun document HTML dans unDocument../aspose.words/document/ objet.
type: docs
weight: 3420
url: /fr/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Permet de spécifier des options supplémentaires lors du chargement d'un document HTML dans un[`Document`](../../aspose.words/document/) objet.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié pour charger un document chiffré. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | Un raccourci pour initialiser une nouvelle instance de cette classe avec des propriétés définies sur les valeurs spécifiées. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus si nécessaire. Peut être une chaîne nulle ou vide. La valeur par défaut est null. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Obtient ou définit une valeur qui spécifie comment les propriétés des éléments de niveau bloc sont importées. La valeur par défaut estMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtient ou définit s'il faut convertir le métafichier (Wmf ouEmf ) images àPng format d'image. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtient ou définit s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut convertir les images SVG chargées au format EMF. La valeur par défaut est`faux` et, si possible, les images SVG chargées sont stockées telles quelles sans conversion. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être nul. La valeur par défaut est null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permet de spécifier les paramètres de police du document. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut ignorer les éléments HTML &lt;noscript&gt;. La valeur par défaut est`faux` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Spécifie le format du document à charger. La valeur par défaut estAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut estWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être une chaîne nulle ou vide. La valeur par défaut est null. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Obtient ou définit le type préféré de nœuds de document qui représenteront les éléments &lt;input&gt; et &lt;select&gt; importés. La valeur par défaut estFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Appelé lors du chargement d'un document et accepte les données sur la progression du chargement. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permet de contrôler le chargement des ressources externes (images, feuilles de style) lorsqu'un document est importé depuis HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Obtient ou définit une valeur indiquant s'il faut prendre en charge les images VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Spécifie s'il faut mettre à jour les champs avec le`sale` attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Appelé lors d'une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Le nombre de millisecondes à attendre avant l'expiration de la requête Web. La valeur par défaut est 100000 millisecondes (100 secondes). |

### Voir également

* class [LoadOptions](../loadoptions/)
* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
