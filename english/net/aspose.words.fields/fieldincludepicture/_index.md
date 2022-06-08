---
title: FieldIncludePicture
second_title: Aspose.Words for .NET API Reference
description: Implements the INCLUDEPICTURE field.
type: docs
weight: 1850
url: /net/aspose.words.fields/fieldincludepicture/
---
## FieldIncludePicture class

Implements the INCLUDEPICTURE field.

```csharp
public class FieldIncludePicture : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldIncludePicture](fieldincludepicture)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [GraphicFilter](../../aspose.words.fields/fieldincludepicture/graphicfilter) { get; set; } | Gets or sets the name of the filter for the format of the graphic that is to be inserted. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLinked](../../aspose.words.fields/fieldincludepicture/islinked) { get; set; } | Gets or sets whether to reduce the file size by not storing graphics data with the document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [ResizeHorizontally](../../aspose.words.fields/fieldincludepicture/resizehorizontally) { get; set; } | Gets or sets whether to resize the picture horizontally from the source. |
| [ResizeVertically](../../aspose.words.fields/fieldincludepicture/resizevertically) { get; set; } | Gets or sets whether to resize the picture vertically from the source. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [SourceFullName](../../aspose.words.fields/fieldincludepicture/sourcefullname) { get; set; } | Gets or sets the location of the picture using an IRI. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
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

Retrieves a picture and displays it as the field result.

## Examples

Shows how to insert images using IMPORT and INCLUDEPICTURE fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two similar field types that we can use to display images linked from the local file system.
// 1 -  The INCLUDEPICTURE field:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Apply the PNG32.FLT filter.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 -  The IMPORT field:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
