---
title: IFieldResultFormatter.format method
linktitle: format method
articleTitle: format method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.IFieldResultFormatter.format method"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Fields/ifieldresultformatter/format/
---

## format(value, format) {#string_generalformat}

Called when Aspose.Words applies a capitalization format switch, i.e. \\\* Upper.


```js
format(value: stringformat: Aspose.Words.Fields.GeneralFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | string |  |
| format | [GeneralFormat](../../generalformat/) |  |

### Remarks

The implementation should return ``null`` to indicate that the default formatting should be applied.



## format(value, format) {#number_generalformat}

Called when Aspose.Words applies a number format switch, i.e. \\\* Ordinal.


```js
format(value: numberformat: Aspose.Words.Fields.GeneralFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | number |  |
| format | [GeneralFormat](../../generalformat/) |  |

### Remarks

The implementation should return ``null`` to indicate that the default formatting should be applied.



## Examples

Shows how to automatically apply a custom format to field results as the fields are updated.

```js
test('FieldResultFormatting', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);
  let formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
  doc.fieldOptions.resultFormatter = formatter;

  // Our field result formatter applies a custom format to newly created fields of three types of formats.
  // Field result formatters apply new formatting to fields as they are updated,
  // which happens as soon as we create them using this InsertField method overload.
  // 1 -  Numeric:
  builder.insertField(" = 2 + 3 \\# $###");

  expect(doc.range.fields.at(0).result).toEqual("$5");
  expect(formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.numeric)).toEqual(1);

  // 2 -  Date/time:
  builder.insertField("DATE \\@ \"d MMMM yyyy\"");

  expect(doc.range.fields.at(1).result.StartsWith("Date: ")).toEqual(true);
  expect(formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.dateTime)).toEqual(1);

  // 3 -  General:
  builder.insertField("QUOTE \"2\" \\* Ordinal");

  expect(doc.range.fields.at(2).result).toEqual("Item # 2:");
  expect(formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.general)).toEqual(1);

  formatter.PrintFormatInvocations();
});


  /// <summary>
  /// When fields with formatting are updated, this formatter will override their formatting
  /// with a custom format, while tracking every invocation.
  /// </summary>
private class FieldResultFormatter : IFieldResultFormatter
{
  public FieldResultFormatter(string numberFormat, string dateFormat, string generalFormat)
  {
    mNumberFormat = numberFormat;
    mDateFormat = dateFormat;
    mGeneralFormat = generalFormat;
  }

  public string FormatNumeric(double value, string format)
  {
    if (string.IsNullOrEmpty(mNumberFormat)) 
      return null;

    string newValue = String.format(mNumberFormat, value);
    FormatInvocations.add(new FormatInvocation(FormatInvocationType.numeric, value, format, newValue));
    return newValue;
  }

  public string FormatDateTime(DateTime value, string format, CalendarType calendarType)
  {
    if (string.IsNullOrEmpty(mDateFormat))
      return null;

    string newValue = String.format(mDateFormat, value);
    FormatInvocations.add(new FormatInvocation(FormatInvocationType.dateTime, `${value} (${calendarType})`, format, newValue));
    return newValue;
  }

  public string Format(string value, GeneralFormat format)
  {
    return Format((object)value, format);
  }

  public string Format(double value, GeneralFormat format)
  {
    return Format((object)value, format);
  }

  private string Format(object value, GeneralFormat format)
  {
    if (string.IsNullOrEmpty(mGeneralFormat))
      return null;

    string newValue = String.format(mGeneralFormat, value);
    FormatInvocations.add(new FormatInvocation(FormatInvocationType.general, value, format.toString(), newValue));
    return newValue;
  }

  public int CountFormatInvocations(FormatInvocationType formatInvocationType)
  {
    if (formatInvocationType == FormatInvocationType.all)
      return FormatInvocations.count;
    return FormatInvocations.count(f => f.FormatInvocationType == formatInvocationType);
  }

  public void PrintFormatInvocations()
  {
    for (let f of FormatInvocations)
      console.log(`Invocation type:\t${f.FormatInvocationType}\n` +
              `\tOriginal value:\t\t${f.value}\n` +
              `\tOriginal format:\t${f.OriginalFormat}\n` +
              `\tNew value:\t\t\t${f.newValue}\n`);
  }

  private readonly string mNumberFormat;
  private readonly string mDateFormat;
  private readonly string mGeneralFormat; 
  private List<FormatInvocation> FormatInvocations { get; } = new aw.Lists.List<FormatInvocation>();

  private class FormatInvocation
  {
    public FormatInvocationType FormatInvocationType { get; }
    public object Value { get; }
    public string OriginalFormat { get; }
    public string NewValue { get; }

    public FormatInvocation(FormatInvocationType formatInvocationType, object value, string originalFormat, string newValue)
    {
      Value = value;
      FormatInvocationType = formatInvocationType;
      OriginalFormat = originalFormat;
      NewValue = newValue;
    }
  }

  public enum FormatInvocationType
  {
    Numeric, DateTime, General, All
  }
}
```

## See Also

* module [Aspose.Words.Fields](../../)
* class [IFieldResultFormatter](../)

