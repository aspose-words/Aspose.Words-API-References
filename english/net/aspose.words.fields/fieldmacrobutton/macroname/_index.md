---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words for .NET
description: Discover the FieldMacroButton MacroName property to easily manage and customize your macros or commands for enhanced functionality and efficiency.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

Gets or sets the name of the macro or command to run.

```csharp
public string MacroName { get; set; }
```

## Examples

Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.That(doc.HasMacros, Is.True);

// Insert a MACROBUTTON field, and reference one of the document's macros by name in the MacroName property.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.That(field.GetFieldCode(), Is.EqualTo(" MACROBUTTON  MyMacro Double click to run macro: MyMacro"));

// Use the property to reference "ViewZoom200", a macro that ships with Microsoft Word.
// We can find all other macros via View -> Macros (dropdown) -> View Macros.
// In that menu, select "Word Commands" from the "Macros in:" drop down.
// If our document contains a custom macro with the same name as a stock macro,
// our macro will be the one that the MACROBUTTON field runs.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.That(field.GetFieldCode(), Is.EqualTo(" MACROBUTTON  ViewZoom200 Run ViewZoom200"));

// Save the document as a macro-enabled document type.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### See Also

* class [FieldMacroButton](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
