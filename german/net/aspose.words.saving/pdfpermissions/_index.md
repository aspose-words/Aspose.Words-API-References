---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.PdfPermissions-Aufzählung zur Steuerung des Benutzerzugriffs auf verschlüsselte PDFs. Erhöhen Sie die Sicherheit und verwalten Sie Dokumentvorgänge effektiv.
type: docs
weight: 6310
url: /de/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Gibt die Vorgänge an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind.

```csharp
[Flags]
public enum PdfPermissions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DisallowAll | `0` | Verbietet alle Vorgänge am PDF-Dokument. Dies ist der Standardwert. |
| AllowAll | `FFFF` | Ermöglicht alle Vorgänge am PDF-Dokument. |
| ContentCopy | `10` | Kopieren oder anderweitiges Extrahieren von Text und Grafiken aus dem Dokument durch andere als die von gesteuertenContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Extrahieren Sie Text und Grafiken (zur Unterstützung der Zugänglichkeit für Benutzer mit Behinderungen oder für andere Zwecke). |
| ModifyContents | `8` | Ändern Sie den Inhalt des Dokuments durch andere als die von gesteuerten Vorgänge.ModifyAnnotations ,FillIn , UndDocumentAssembly . |
| ModifyAnnotations | `20` | Textanmerkungen hinzufügen oder ändern, interaktive Formularfelder ausfüllen und, fallsModifyContents ist auch das Festlegen, Erstellen oder Ändern interaktiver Formularfelder (einschließlich Signaturfelder). |
| FillIn | `100` | Füllen Sie vorhandene interaktive Formularfelder (einschließlich Signaturfelder) aus, auch wennModifyContents ist klar. |
| DocumentAssembly | `400` | Das Dokument zusammenstellen (Seiten einfügen, drehen oder löschen und Dokumentgliederungselemente oder Miniaturansichten erstellen), auch wennModifyContents ist klar. |
| Printing | `4` | Drucken Sie das Dokument (möglicherweise nicht in der höchsten Qualitätsstufe, je nachdem, ob HighResolutionPrinting ist ebenfalls eingestellt). |
| HighResolutionPrinting | `804` | Drucken Sie das Dokument in eine Darstellung, aus der eine originalgetreue digitale Kopie des PDF-Inhalts generiert werden kann, basierend auf einem implementierungsabhängigen Algorithmus. Wenn dieses Flag gelöscht ist (und Printing gesetzt ist), soll der Druck auf eine einfache Darstellung des Erscheinungsbilds beschränkt sein, möglicherweise in verschlechterter Qualität. |

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
