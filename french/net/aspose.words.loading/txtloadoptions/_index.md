---
title: TxtLoadOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Permet de spécifier des options supplémentaires lors du chargementText document dans unDocument../aspose.words/document objet.
type: docs
weight: 3530
url: /fr/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Permet de spécifier des options supplémentaires lors du chargementText document dans un[`Document`](../../aspose.words/document) objet.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [TxtLoadOptions](txtloadoptions)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus si nécessaire. Peut être une chaîne nulle ou vide. La valeur par défaut est null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Obtient ou définit s'il faut convertir le métafichier (Wmf ouEmf ) images àPng format d'image. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | Obtient ou définit s'il faut convertir les formes avec EquationXML en objets Office Math. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces) { get; set; } | Permet de spécifier comment les éléments de la liste numérotée sont reconnus lorsqu'un document est importé à partir d'un format texte brut. La valeur par défaut est true. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection) { get; set; } | Obtient ou définit une direction de document. La valeur par défaut estLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être nul. La valeur par défaut est null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Permet de spécifier les paramètres de police du document. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions) { get; set; } | Obtient ou définit l'option préférée d'un espace de tête. La valeur par défaut estConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Spécifie le format du document à charger. La valeur par défaut estAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut estWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être une chaîne nulle ou vide. La valeur par défaut est null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Appelé lors du chargement d'un document et accepte les données sur la progression du chargement. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Permet de contrôler le chargement des ressources externes (images, feuilles de style) lorsqu'un document est importé depuis HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions) { get; set; } | Obtient ou définit l'option préférée de gestion des espaces de fin. La valeur par défaut estTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Spécifie s'il faut mettre à jour les champs avec le`sale` attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Appelé lors d'une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |

### Voir également

* class [LoadOptions](../loadoptions)
* espace de noms [Aspose.Words.Loading](../../aspose.words.loading)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
