---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources méthode"
linktitle: "get_ExportFontResources"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources. Spécifie si les ressources de police doivent être exportées vers HTML, MHTML ou EPUB. La valeur par défaut est false en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Spécifie si les ressources de police doivent être exportées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Remarques


L'exportation des ressources de police permet un rendu de document cohérent, indépendant des polices disponibles dans l'environnement d'un utilisateur donné.

Si [ExportFontResources](./) est défini sur **true**, le document HTML principal fera référence à chaque police via la règle d'annotation CSS 3 **%@font-face** et les polices seront générées en fichiers séparés. Lors de l'exportation vers les formats IDPF EPUB ou MHTML, les polices seront intégrées dans le package correspondant ainsi que les autres fichiers annexes.

Si [ExportFontsAsBase64](../get_exportfontsasbase64/) est défini sur **true**, les polices ne seront pas enregistrées dans des fichiers séparés. À la place, elles seront intégrées dans les règles **%@font-face** en encodage Base64.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
