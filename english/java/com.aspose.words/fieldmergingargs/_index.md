---
title: FieldMergingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the MergeField event.
type: docs
weight: 218
url: /java/com.aspose.words/fieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class FieldMergingArgs extends FieldMergingArgsBase
```

Provides data for the **MergeField** event.

To learn more, visit the **Mail Merge and Reporting** documentation article.

The **MergeField** event occurs during mail merge when a simple mail merge field is encountered in the document. You can respond to this event to return text for the mail merge engine to insert into the document.
## Methods

| Method | Description |
| --- | --- |
| [getText()](#getText--) | Gets the text that will be inserted into the document for the current merge field. |
| [setText(String value)](#setText-java.lang.String-) | Sets the text that will be inserted into the document for the current merge field. |
### getText() {#getText--}
```
public String getText()
```


Gets the text that will be inserted into the document for the current merge field.

When your event handler is called, this property is set to null.

If you leave Text as null, the mail merge engine will insert [FieldMergingArgsBase.getFieldValue()](../../com.aspose.words/fieldmergingargsbase\#getFieldValue--) / [FieldMergingArgsBase.setFieldValue(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase\#setFieldValue-java.lang.Object-) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.

**Returns:**
java.lang.String - The text that will be inserted into the document for the current merge field.
### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Sets the text that will be inserted into the document for the current merge field.

When your event handler is called, this property is set to null.

If you leave Text as null, the mail merge engine will insert [FieldMergingArgsBase.getFieldValue()](../../com.aspose.words/fieldmergingargsbase\#getFieldValue--) / [FieldMergingArgsBase.setFieldValue(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase\#setFieldValue-java.lang.Object-) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text that will be inserted into the document for the current merge field. |

