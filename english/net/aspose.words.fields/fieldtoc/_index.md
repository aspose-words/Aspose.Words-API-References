---
title: FieldToc
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 2340
url: /net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implements the TOC field.

```csharp
public class FieldToc : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldToc](fieldtoc)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname) { get; set; } | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel) { get; set; } | Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles) { get; set; } | Gets or sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier) { get; set; } | Gets or sets a string that should match type identifiers of TC fields being included. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange) { get; set; } | Gets or sets a range of levels of the table of contents entries to be included. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator) { get; set; } | Gets or sets a sequence of characters that separate an entry and its page number. |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange) { get; set; } | Gets or sets a range of heading levels to include. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout) { get; set; } | Gets or sets whether to hide tab leader and page numbers in Web layout view. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks) { get; set; } | Gets or sets whether to make the table of contents entries hyperlinks. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange) { get; set; } | Gets or sets a range of levels of the table of contents entries from which to omits page numbers. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier) { get; set; } | Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks) { get; set; } | Gets or sets whether to preserve newline characters within table entries. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs) { get; set; } | Gets or sets whether to preserve tab entries within table entries. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator) { get; set; } | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel) { get; set; } | Gets or sets the name of the sequence identifier used when building a table of figures. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Gets the Microsoft Word field type. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel) { get; set; } | Gets or sets whether to use the applied paragraph outline level. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update)(bool) | Performs a field update. Throws if the field is being updated already. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers)() | Updates the page numbers for items in this table of contents. |

### Remarks

Builds a table of contents (which can also be a table of figures) using the entries specified by TC fields, their heading levels, and specified styles, and inserts that table at this place in the document.

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
