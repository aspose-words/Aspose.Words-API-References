---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words för .NET
description: Ta enkelt bort hela formulärfält med metoden FormField RemoveField, vilket förbättrar dokumentets tydlighet och organisation.
type: docs
weight: 240
url: /sv/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Tar bort hela formulärfältet, inte bara specialtecknet för formulärfältet.

```csharp
public void RemoveField()
```

## Anmärkningar

Om det finns ett bokmärke kopplat till formulärfältet tas bokmärket inte bort.

## Exempel

Visar hur man tar bort ett formulärfält.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Se även

* class [FormField](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
