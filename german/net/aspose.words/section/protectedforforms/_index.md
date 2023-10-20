---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words für .NET
description: Section ProtectedForForms eigendom. True wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist können Benutzer Text nur in Formularfeldern in Microsoft Word auswählen und ändern in C#.
type: docs
weight: 60
url: /de/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

True, wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist, können Benutzer Text nur in Formularfeldern in Microsoft Word auswählen und ändern.

```csharp
public bool ProtectedForForms { get; set; }
```

## Beispiele

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

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
