---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode méthode"
linktitle: "get_DateTimeParsingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode méthode. Obtient ou définit le mode qui spécifie comment le texte du document est analysé pour identifier les valeurs de date et d’heure. La valeur par défaut est UseCurrentLocale en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Obtient ou définit le mode qui spécifie comment le texte du document est analysé pour identifier les valeurs de date et d’heure. La valeur par défaut est [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


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

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
