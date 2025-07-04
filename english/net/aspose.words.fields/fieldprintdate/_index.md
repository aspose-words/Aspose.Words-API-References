---
title: FieldPrintDate Class
linktitle: FieldPrintDate
articleTitle: FieldPrintDate
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldPrintDate class to effortlessly implement the PRINTDATE field, enhancing document automation and efficiency.
type: docs
weight: 2690
url: /net/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class

Implements the PRINTDATE field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldPrintDate : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldPrintDate](fieldprintdate/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |
| [UseLunarCalendar](../../aspose.words.fields/fieldprintdate/uselunarcalendar/) { get; set; } | Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldprintdate/usesakaeracalendar/) { get; set; } | Gets or sets whether to use the Saka Era calendar. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldprintdate/useumalquracalendar/) { get; set; } | Gets or sets whether to use the Um-al-Qura calendar. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Retrieves the date and time on which the document was last printed. By default, the Gregorian calendar is used.

## Examples

Shows read PRINTDATE fields.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// When a document is printed by a printer or printed as a PDF (but not exported to PDF),
// PRINTDATE fields will display the print operation's date/time.
// If no printing has taken place, these fields will display "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.That(field.Result, Is.EqualTo("3/25/2020 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE "));

// Below are three different calendar types according to which the PRINTDATE field
// can display the date and time of the last printing operation.
// 1 -  Islamic Lunar Calendar:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.That(field.UseLunarCalendar, Is.True);
Assert.That(field.Result, Is.EqualTo("8/1/1441 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE  \\h"));

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 -  Umm al-Qura calendar:
Assert.That(field.UseUmAlQuraCalendar, Is.True);
Assert.That(field.Result, Is.EqualTo("8/1/1441 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE  \\u"));

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 -  Indian National Calendar:
Assert.That(field.UseSakaEraCalendar, Is.True);
Assert.That(field.Result, Is.EqualTo("1/5/1942 12:00:00 AM"));
Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINTDATE  \\s"));
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
