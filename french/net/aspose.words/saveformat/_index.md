---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.SaveFormat pour choisir facilement les formats d'enregistrement de documents, améliorant ainsi la gestion de vos fichiers et la compatibilité pour des flux de travail transparents.
type: docs
weight: 5580
url: /fr/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Indique le format dans lequel le document est enregistré.

```csharp
public enum SaveFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Unknown | `0` | Valeur par défaut, non valide pour le format de fichier. |
| Doc | `10` | Enregistre le document au format de document Microsoft Word 97 - 2007. |
| Dot | `11` | Enregistre le document au format de modèle Microsoft Word 97 - 2007. |
| Docx | `20` | Enregistre le document en tant que document WordprocessingML Office Open XML (sans macro). |
| Docm | `21` | Enregistre le document en tant que document Office Open XML WordprocessingML prenant en charge les macros. |
| Dotx | `22` | Enregistre le document en tant que modèle WordprocessingML Office Open XML (sans macro). |
| Dotm | `23` | Enregistre le document en tant que modèle Office Open XML WordprocessingML prenant en charge les macros. |
| FlatOpc | `24` | Enregistre le document au format Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcMacroEnabled | `25` | Enregistre le document en tant que document Office Open XML WordprocessingML Macro-Enabled stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplate | `26` | Enregistre le document en tant que modèle WordprocessingML Office Open XML (sans macro) stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Enregistre le document en tant que modèle Office Open XML WordprocessingML Macro-Enabled stocké dans un fichier XML plat au lieu d'un package ZIP. |
| Rtf | `30` | Enregistre le document au format RTF. Tous les caractères supérieurs à 7 bits sont échappés sous forme de caractères hexadécimaux ou Unicode. |
| WordML | `31` | Enregistre le document au format Microsoft Word 2003 WordprocessingML. |
| Pdf | `40` | Enregistre le document au format PDF (Adobe Portable Document). |
| Xps | `41` | Enregistre le document au format XPS (XML Paper Specification). |
| XamlFixed | `42` | Enregistre le document au format XAML (Extensible Application Markup Language) en tant que document fixe. |
| Svg | `44` | Enregistre le document au format Svg (Scalable Vector Graphics). |
| HtmlFixed | `45` | Enregistre le document au format HTML en utilisant des éléments positionnés de manière absolue |
| OpenXps | `46` | Enregistre le document au format OpenXPS (Ecma-388). |
| Ps | `47` | Enregistre le document au format PS (PostScript). |
| Pcl | `48` | Enregistre le document au format PCL (Printer Control Language). |
| Html | `50` | Enregistre le document au format HTML. |
| Mhtml | `51` | Enregistre le document au format MHTML (archive Web). |
| Epub | `52` | Enregistre le document au format EPUB. |
| Azw3 | `53` | Enregistre le document au format AZW3. |
| Mobi | `54` | Enregistre le document au format MOBI. |
| Odt | `60` | Enregistre le document en tant que document texte ODF. |
| Ott | `61` | Enregistre le document en tant que modèle de document texte ODF. |
| Text | `70` | Enregistre le document au format texte brut. |
| XamlFlow | `71` | **Bêta.** Enregistre le document au format XAML (Extensible Application Markup Language) en tant que document de flux. |
| XamlFlowPack | `72` | **Bêta.** Enregistre le document au format de package Extensible Application Markup Language (XAML) en tant que document de flux. |
| Markdown | `73` | Enregistre le document au format Markdown. |
| Xlsx | `80` | Enregistre le document en tant que document Office Open XML SpreadsheetML (sans macro). |
| Tiff | `100` | Affiche une ou plusieurs pages du document et les enregistre dans un fichier TIFF d'une ou plusieurs pages. |
| Png | `101` | Affiche une page du document et l'enregistre sous forme de fichier PNG. |
| Bmp | `102` | Affiche une page du document et l'enregistre sous forme de fichier BMP. |
| Emf | `103` | Affiche une page du document et l'enregistre sous forme de fichier vectoriel EMF (Enhanced Meta File). |
| Jpeg | `104` | Affiche une page du document et l'enregistre sous forme de fichier JPEG. |
| Gif | `105` | Affiche une page du document et l'enregistre sous forme de fichier GIF. |
| Eps | `106` | Affiche une page du document et l'enregistre sous forme de fichier EPS. |
| WebP | `107` | Affiche une page du document et l'enregistre sous forme de fichier WebP. |

## Exemples

Montre comment convertir du format DOCX au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Voir également

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
