---
title: Class PdfEncryptionDetails
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfEncryptionDetails klas. Enthält Details zur Verschlüsselung und Zugriffsberechtigungen für ein PDFDokument.
type: docs
weight: 5180
url: /de/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Enthält Details zur Verschlüsselung und Zugriffsberechtigungen für ein PDF-Dokument.

```csharp
public class PdfEncryptionDetails
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/)(string, string) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Gibt das Besitzerkennwort für das verschlüsselte PDF-Dokument an. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Gibt die Operationen an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert istDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Gibt das Benutzerkennwort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist. |

### Beispiele

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Beginnen Sie damit, alle Berechtigungen zu verweigern.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Berechtigungen erweitern, um die Bearbeitung von Anmerkungen zu ermöglichen.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Verschlüsselung über die Eigenschaft "EncryptionDetails" aktivieren.
saveOptions.EncryptionDetails = encryptionDetails;

// Wenn wir dieses Dokument öffnen, müssen wir das Passwort angeben, bevor wir auf seinen Inhalt zugreifen können.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


