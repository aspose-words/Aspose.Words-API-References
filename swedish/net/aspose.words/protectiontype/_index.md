---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ProtectionType-enum för robust dokumentsäkerhet. Förbättra dina dokument med anpassningsbara skyddsalternativ idag!
type: docs
weight: 5240
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
| AllowOnlyFormFields | `2` | Användaren kan bara ange data i formulärfälten i dokumentet. |
| AllowOnlyRevisions | `0` | Användaren kan bara lägga till revisionsmarkeringar i dokumentet. |
| ReadOnly | `3` | Inga ändringar är tillåtna i dokumentet. Tillgängligt sedan Microsoft Word 2003. |
| NoProtection | `-1` | Dokumentet är inte skyddat. |

## Exempel

Visar hur man stänger av skyddet för en sektion.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Tillämpa skrivskydd på varje avsnitt i dokumentet.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Stäng av skrivskyddet för den första sektionen.
doc.Sections[0].ProtectedForForms = false;

// I detta utdatadokument kommer vi att kunna redigera det första avsnittet fritt,
// och vi kommer bara att kunna redigera innehållet i formulärfältet i den andra sektionen.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
