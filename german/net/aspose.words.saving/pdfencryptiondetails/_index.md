---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.PdfEncryptionDetails klas. Enthält Details zur Verschlüsselung und Zugriffsberechtigungen für ein PDFDokument in C#.
type: docs
weight: 5460
url: /de/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Enthält Details zur Verschlüsselung und Zugriffsberechtigungen für ein PDF-Dokument.

Um mehr zu erfahren, besuchen Sie die[Schützen oder verschlüsseln Sie ein Dokument](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) Dokumentationsartikel.

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
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Gibt die Vorgänge an, die einem Benutzer für ein verschlüsseltes PDF-Dokument gestattet sind. Der Standardwert istDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist. |

## Beispiele

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Berechtigungen erweitern, um das Bearbeiten von Anmerkungen zu ermöglichen.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Verschlüsselung über die Eigenschaft „EncryptionDetails“ aktivieren.
saveOptions.EncryptionDetails = encryptionDetails;

// Wenn wir dieses Dokument öffnen, müssen wir das Passwort angeben, bevor wir auf den Inhalt zugreifen können.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
