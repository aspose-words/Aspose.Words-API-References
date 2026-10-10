---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::SaveFormat enum. Indique le format dans lequel le document est enregistré en C++."
type: docs
weight: 114000
url: /fr/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Indique le format dans lequel le document est enregistré.

```cpp
enum class SaveFormat
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Inconnu | 0 | Par défaut, valeur invalide pour le format de fichier. |
| Doc | 10 | Enregistre le document au format Microsoft Word 97 - 2007 [Document](../document/). |
| Dot | 11 | Enregistre le document au format Modèle Microsoft Word 97 - 2007. |
| Docx | 20 | Enregistre le document en tant que [Document](../document/) Office Open XML WordprocessingML (sans macro). |
| Docm | 21 | Enregistre le document en tant que [Document](../document/) Office Open XML WordprocessingML avec macros. |
| Dotx | 22 | Enregistre le document en tant que Modèle Office Open XML WordprocessingML (sans macro). |
| Dotm | 23 | Enregistre le document en tant que Modèle Office Open XML WordprocessingML avec macros. |
| FlatOpc | 24 | Enregistre le document en tant que Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcMacroEnabled | 25 | Enregistre le document en tant que [Document](../document/) Office Open XML WordprocessingML avec macros stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplate | 26 | Enregistre le document en tant que Modèle Office Open XML WordprocessingML (sans macro) stocké dans un fichier XML plat au lieu d'un package ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | Enregistre le document en tant que Modèle Office Open XML WordprocessingML avec macros stocké dans un fichier XML plat au lieu d'un package ZIP. |
| Rtf | 30 | Enregistre le document au format RTF. Tous les caractères supérieurs à 7 bits sont échappés en hexadécimal ou en caractères Unicode. |
| WordML | 31 | Enregistre le document au format Microsoft Word 2003 WordprocessingML. |
| Pdf | 40 | Enregistre le document au format PDF (Adobe Portable [Document](../document/)). |
| Xps | 41 | Enregistre le document au format XPS (XML Paper Specification). |
| XamlFixed | 42 | Enregistre le document au format Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) en tant que document fixe. |
| Svg | 44 | Enregistre le document au format Svg (Scalable Vector Graphics). |
| HtmlFixed | 45 | Enregistre le document au format HTML en utilisant des éléments positionnés absolument. |
| OpenXps | 46 | Enregistre le document au format OpenXPS (Ecma-388). |
| Ps | 47 | Enregistre le document au format PS (PostScript). |
| Pcl | 48 | Enregistre le document au format PCL (Printer Control Language). |
| Html | 50 | Enregistre le document au format HTML. |
| Mhtml | 51 | Enregistre le document au format MHTML (Web archive). |
| Epub | 52 | Enregistre le document au format EPUB. |
| Azw3 | 53 | Enregistre le document au format AZW3. |
| Mobi | 54 | Enregistre le document au format MOBI. |
| Odt | 60 | Enregistre le document en tant que ODF Text [Document](../document/). |
| Ott | 61 | Enregistre le document en tant que modèle ODF Text [Document](../document/). |
| Texte | 70 | Enregistre le document au format texte brut. |
| XamlFlow | 71 | **Beta.** Enregistre le document au format Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) en tant que document flux. |
| XamlFlowPack | 72 | **Beta.** Enregistre le document au format Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) package format en tant que document flux. |
| Markdown | 73 | Enregistre le document au format Markdown. |
| Xlsx | 80 | Enregistre le document en tant que Office Open XML SpreadsheetML [Document](../document/) (sans macro). |
| Docling | 81 | Enregistre le document au format Docling JSON. |
| Tiff | 100 | Rend une ou plusieurs pages du document et les enregistre dans un fichier TIFF simple ou multipage. |
| Png | 101 | Rend une page du document et l’enregistre sous forme de fichier PNG. |
| Bmp | 102 | Rend une page du document et l’enregistre sous forme de fichier BMP. |
| Emf | 103 | Rend une page du document et l’enregistre sous forme de fichier EMF vectoriel (Enhanced Meta File). |
| Jpeg | 104 | Rend une page du document et l’enregistre sous forme de fichier JPEG. |
| Gif | 105 | Rend une page du document et l’enregistre sous forme de fichier GIF. |
| Eps | 106 | Rend une page du document et l’enregistre sous forme de fichier EPS. |


## Exemples



Montre comment convertir du format DOCX vers le format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
