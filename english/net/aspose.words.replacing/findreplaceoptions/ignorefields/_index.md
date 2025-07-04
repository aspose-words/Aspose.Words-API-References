---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words for .NET
description: Discover the FindReplaceOptions IgnoreFields property to easily manage text within fields. Control when to ignore content for efficient searching!
type: docs
weight: 80
url: /net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Gets or sets a boolean value indicating either to ignore text inside fields. The default value is `false`.

```csharp
public bool IgnoreFields { get; set; }
```

## Remarks

This option affects whole field (all nodes between FieldStart and FieldEnd).

To ignore only field codes, please use corresponding option [`IgnoreFieldCodes`](../ignorefieldcodes/).

## Examples

Shows how to ignore text inside fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "IgnoreFields" flag to "true" to get the find-and-replace
// operation to ignore text inside fields.
// Set the "IgnoreFields" flag to "false" to get the find-and-replace
// operation to also search for text inside fields.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.That(doc.GetText().Trim(), Is.EqualTo(ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"));
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
