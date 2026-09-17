---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XxlsxDateTimeParsingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure en C++."
type: docs
weight: 86500
url: /fr/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure.

```cpp
enum class XlsxDateTimeParsingMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| UseCurrentLocale | 0 | Le format datetime défini pour le thread actuel est d'abord utilisé pour analyser les valeurs de chaîne. Si l'analyse échoue, d'autres formats datetime courants sont essayés. |
| Auto | 1 | Le format datetime utilisé dans un document est déterminé automatiquement. Cela peut prendre du temps supplémentaire. |


## Exemples



Montre comment spécifier l'autodétection du format date‑heure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Spécifiez l'utilisation de l'autodétection du format datetime.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
