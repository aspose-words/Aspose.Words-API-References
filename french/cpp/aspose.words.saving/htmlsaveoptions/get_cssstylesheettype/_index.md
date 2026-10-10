---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType méthode"
linktitle: "get_CssStyleSheetType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType méthode. Spécifie comment les styles CSS (Cascading Style Sheet) sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut est Inline pour HTML/MHTML et External pour EPUB en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


Spécifie comment les styles CSS (Cascading [Style](../../../aspose.words/style/) Sheet) sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut est [Inline](../../cssstylesheettype/) pour HTML/MHTML et [External](../../cssstylesheettype/) pour EPUB.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Remarques


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## Voir aussi

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
