---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.PdfEncryptionDetails für sichere PDF-Verschlüsselung und anpassbare Zugriffsberechtigungen, um sicherzustellen, dass Ihre Dokumente geschützt bleiben.
type: docs
weight: 6250
url: /de/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Enthält Details zur Verschlüsselung und Zugriffsberechtigungen für ein PDF-Dokument.

Um mehr zu erfahren, besuchen Sie die[Schützen oder Verschlüsseln eines Dokuments](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) Dokumentationsartikel.

```csharp
public class PdfEncryptionDetails
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | Initialisiert eine Instanz dieser Klasse. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Gibt das Besitzerkennwort für das verschlüsselte PDF-Dokument an. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Gibt die Operationen an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert istDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Gibt das Benutzerkennwort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist. |

## Beispiele

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Erweitern Sie die Berechtigungen, um das Bearbeiten von Anmerkungen zu ermöglichen.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Aktivieren Sie die Verschlüsselung über die Eigenschaft „EncryptionDetails“.
saveOptions.EncryptionDetails = encryptionDetails;

// Wenn wir dieses Dokument öffnen, müssen wir das Passwort eingeben, bevor wir auf seinen Inhalt zugreifen können.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
