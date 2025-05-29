---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die UserPassword-Eigenschaft die PDF-Sicherheit verbessert, indem sie für den Zugriff ein Kennwort erfordert und so sicherstellt, dass Ihre Dokumente geschützt und vertraulich bleiben.
type: docs
weight: 40
url: /de/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Gibt das Benutzerkennwort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist.

```csharp
public string UserPassword { get; set; }
```

## Bemerkungen

Das Benutzerkennwort wird benötigt, um ein verschlüsseltes PDF-Dokument zur Ansicht zu öffnen. Die in angegebenen Berechtigungen[`Permissions`](../permissions/) wird von der Lesesoftware erzwungen.

Das Benutzerkennwort kann`null` oder eine leere Zeichenfolge. In diesem Fall wird beim Öffnen des PDF-Dokuments kein Kennwort vom Benutzer abgefragt. Das Benutzerkennwort darf nicht mit dem Eigentümerkennwort identisch sein.

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

* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
