---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Spécifie comment Aspose.Words exporte OfficeMath en texte en C++."
type: docs
weight: 86250
url: /fr/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Spécifie comment Aspose.Words exporte OfficeMath vers [Texte](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Texte | 0 | Exportez OfficeMath en texte brut. |
| Latex | 3 | Exportez OfficeMath en LaTeX. |


## Exemples



Montre comment exporter l'objet OfficeMath en Latex dans un fichier TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
