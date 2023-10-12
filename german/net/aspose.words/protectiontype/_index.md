---
title: Enum ProtectionType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ProtectionType opsomming. Schutztyp für ein Dokument.
type: docs
weight: 4510
url: /de/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Schutztyp für ein Dokument.

```csharp
public enum ProtectionType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AllowOnlyComments | `1` | Der Benutzer kann nur Kommentare im Dokument ändern. |
| AllowOnlyFormFields | `2` | Der Benutzer kann nur Daten in die Formularfelder im Dokument eingeben. |
| AllowOnlyRevisions | `0` | Der Benutzer kann dem Dokument nur Revisionsmarkierungen hinzufügen. |
| ReadOnly | `3` | Es sind keine Änderungen am Dokument zulässig. Verfügbar seit Microsoft Word 2003. |
| NoProtection | `-1` | Das Dokument ist nicht geschützt. |

### Beispiele

Zeigt, wie der Schutz für einen Abschnitt deaktiviert wird.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Schreibschutz auf jeden Abschnitt im Dokument anwenden.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Schreibschutz für den ersten Abschnitt deaktivieren.
doc.Sections[0].ProtectedForForms = false;

// In diesem Ausgabedokument können wir den ersten Abschnitt frei bearbeiten,
// und wir können den Inhalt des Formularfelds nur im zweiten Abschnitt bearbeiten.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


