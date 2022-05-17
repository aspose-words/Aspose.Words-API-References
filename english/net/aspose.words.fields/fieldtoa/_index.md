---
title: FieldToa
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 2330
url: /net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implements the TOA field.

```csharp
public class FieldToa : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldToa](fieldtoa)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname) { get; set; } | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory) { get; set; } | Gets or sets the integral category for entries included in the table. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator) { get; set; } | Gets or sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator) { get; set; } | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator) { get; set; } | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting) { get; set; } | Gets or sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename) { get; set; } | Gets or sets the name of a sequence whose number is included with the page number. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator) { get; set; } | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Gets the Microsoft Word field type. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading) { get; set; } | Gets or sets whether to include the category heading for the entries in a table of authorities. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim) { get; set; } | Gets or sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update)(bool) | Performs a field update. Throws if the field is being updated already. |

### Remarks

Builds a table of authorities (that is, a list of the references in a legal document, such as references to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the entries specified by TA fields.

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
