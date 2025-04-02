---
title: FieldUpdateCultureSource enumeration
linktitle: FieldUpdateCultureSource enumeration
articleTitle: FieldUpdateCultureSource enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.FieldUpdateCultureSource enumeration. Indicates what culture to use during field update."
type: docs
weight: 1090
url: /nodejs-net/Aspose.Words.Fields/fieldupdateculturesource/
---

## FieldUpdateCultureSource enumeration

Indicates what culture to use during field update.


### Members

| Name | Description |
| --- | --- |
| CurrentThread | The culture of the current execution thread is used to update fields. |
| FieldCode | The culture specified in the field formatting properties via language setting is used. |

### Examples

Shows how to specify the source of the culture used for date formatting during a field update or mail merge.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert two merge fields with German locale.
builder.font.localeId = new CultureInfo("de-DE").LCID;
builder.insertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.write(" - ");
builder.insertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Set the current culture to US English after preserving its original value in a variable.
CultureInfo currentCulture = Thread.currentThread.CurrentCulture;
Thread.currentThread.CurrentCulture = new CultureInfo("en-US");

// This merge will use the current thread's culture to format the date, US English.
doc.mailMerge.execute(new.at(] { "Date1" }, new object[) { new DateTime(2020, 1, 01) });

// Configure the next merge to source its culture value from the field code. The value of that culture will be German.
doc.fieldOptions.fieldUpdateCultureSource = aw.Fields.FieldUpdateCultureSource.FieldCode;
doc.mailMerge.execute(new.at(] { "Date2" }, new object[) { new DateTime(2020, 1, 01) });

// The first merge result contains a date formatted in English, while the second one is in German.
expect(doc.range.text.trim()).toEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020");

// Restore the thread's original culture.
Thread.currentThread.CurrentCulture = currentCulture;
```

### See Also

* module [Aspose.Words.Fields](../)

