---
title: FieldIndex
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1870
url: /net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implements the INDEX field.

```csharp
public class FieldIndex : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldIndex](fieldindex)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname) { get; set; } | Gets or sets the name of the bookmark that marks the portion of the document used to build the index. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator) { get; set; } | Gets or sets the character sequence that is used to separate cross references and other entries. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype) { get; set; } | Gets or sets an index entry type used to build the index. |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator) { get; } | Gets a value indicating whether a page number separator is overridden through the field's code. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename) { get; } | Gets a value indicating whether a sequence should be used while the field's result building. |
| [Heading](../../aspose.words.fields/fieldindex/heading) { get; set; } | Gets or sets a heading that appears at the start of each set of entries for any given letter. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid) { get; set; } | Gets or sets the language ID used to generate the index. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange) { get; set; } | Gets or sets a range of letters to which limit the index. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns) { get; set; } | Gets or sets the number of columns per page used when building the index. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator) { get; set; } | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator) { get; set; } | Gets or sets the character sequence that is used to separate an index entry and its page number. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator) { get; set; } | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline) { get; set; } | Gets or sets whether run subentries into the same line as the main entry. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename) { get; set; } | Gets or sets the name of a sequence whose number is included with the page number. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator) { get; set; } | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Gets the Microsoft Word field type. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi) { get; set; } | Gets or sets whether to enable the use of yomi text for index entries. |

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

Builds an index using the index entries specified by XE fields, and inserts that index at this place in the document.

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
