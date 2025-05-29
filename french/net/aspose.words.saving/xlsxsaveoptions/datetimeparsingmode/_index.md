---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété DateTimeParsingMode de XlsxSaveOptions pour personnaliser la façon dont votre document analyse les dates et les heures, garantissant ainsi une interprétation précise des données.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Obtient ou définit le mode qui spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure. La valeur par défaut estUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

## Exemples

Montre comment spécifier la détection automatique du format de date et d'heure.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Spécifiez en utilisant la détection automatique du format datetime.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Voir également

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
