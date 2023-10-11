---
title: Enum ProtectionType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.ProtectionType uppräkning. Skyddstyp för ett dokument.
type: docs
weight: 4510
url: /sv/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Skyddstyp för ett dokument.

```csharp
public enum ProtectionType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AllowOnlyComments | `1` | Användaren kan bara ändra kommentarer i dokumentet. |
| AllowOnlyFormFields | `2` | Användaren kan endast ange data i formulärfälten i dokumentet. |
| AllowOnlyRevisions | `0` | Användaren kan bara lägga till revisionsmärken till dokumentet. |
| ReadOnly | `3` | Inga ändringar är tillåtna i dokumentet. Tillgänglig sedan Microsoft Word 2003. |
| NoProtection | `-1` | Dokumentet är inte skyddat. |

### Exempel

Visar hur man stänger av skyddet för en sektion.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Använd skrivskydd på varje avsnitt i dokumentet.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Stäng av skrivskyddet för det första avsnittet.
doc.Sections[0].ProtectedForForms = false;

// I detta utdatadokument kommer vi att kunna redigera det första avsnittet fritt,
// och vi kommer bara att kunna redigera innehållet i formulärfältet i det andra avsnittet.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


