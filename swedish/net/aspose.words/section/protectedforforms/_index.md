---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ProtectedForForms i Microsoft Word förbättrar dokumentsäkerheten, vilket gör att användare enkelt kan redigera endast angivna formulärfält.
type: docs
weight: 60
url: /sv/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Sant om avsnittet är skyddat för formulär. När ett avsnitt är skyddat för formulär kan användare endast markera och ändra text i formulärfält i Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

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

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
