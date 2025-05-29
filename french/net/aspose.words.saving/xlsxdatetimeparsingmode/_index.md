---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération XlsxDateTimeParsingMode d'Aspose.Words pour une analyse efficace du texte de vos documents. Identifiez facilement les valeurs de date et d'heure dans vos fichiers !
type: docs
weight: 6510
url: /fr/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure.

```csharp
public enum XlsxDateTimeParsingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| UseCurrentLocale | `0` | Le format de date/heure défini pour le thread actuel est utilisé en premier pour analyser les valeurs de chaîne. En cas d'échec, d'autres formats de date/heure courants sont essayés. |
| Auto | `1` | Le format de date/heure utilisé dans un document est déterminé automatiquement. Cette opération peut prendre plus de temps. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
