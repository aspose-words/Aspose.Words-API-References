---
title: FieldHyperlink
second_title: Aspose.Words for .NET API Reference
description: Implements the HYPERLINK field
type: docs
weight: 1840
url: /net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

Implements the HYPERLINK field

```csharp
public class FieldHyperlink : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldHyperlink](fieldhyperlink)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address) { get; set; } | Gets or sets a location where this hyperlink jumps. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap) { get; set; } | Gets or sets whether to append coordinates to the hyperlink for a server-side image map. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow) { get; set; } | Gets or sets whether to open the destination site in a new web browser window. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip) { get; set; } | Gets or sets the ScreenTip text for the hyperlink. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress) { get; set; } | Gets or sets a location in the file, such as a bookmark, where this hyperlink jumps. |
| [Target](../../aspose.words.fields/fieldhyperlink/target) { get; set; } | Gets or sets the target to which the link should be redirected. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update)(bool) | Performs a field update. Throws if the field is being updated already. |

## Remarks

When selected, causes control to jump to the location such as a bookmark or a URL.

## Examples

Shows how to use HYPERLINK fields to link to documents in the local file system.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document and then place the cursor at the specified bookmark.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// When we click this HYPERLINK field in Microsoft Word,
// it will open the linked document, and automatically scroll down to the specified iframe.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
