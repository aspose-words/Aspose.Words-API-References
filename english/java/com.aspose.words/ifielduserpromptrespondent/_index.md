---
title: IFieldUserPromptRespondent
linktitle: IFieldUserPromptRespondent
second_title: Aspose.Words for Java
description: Represents the respondent to user prompts during field update in Java.
type: docs
weight: 666
url: /java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface IFieldUserPromptRespondent
```

Represents the respondent to user prompts during field update.

 **Remarks:** 

The ASK and FILLIN fields are the examples of fields that prompt the user for some response. Implement this interface and assign it to the [FieldOptions.getUserPromptRespondent()](../../com.aspose.words/fieldoptions/\#getUserPromptRespondent) / [FieldOptions.setUserPromptRespondent(com.aspose.words.IFieldUserPromptRespondent)](../../com.aspose.words/fieldoptions/\#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent) property to establish interaction between field update and the user.

 **Examples:** 

Shows how to create an ASK field, and set its properties.

```

 public void fieldAsk() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Place a field where the response to our ASK field will be placed.
     FieldRef fieldRef = (FieldRef) builder.insertField(FieldType.FIELD_REF, true);
     fieldRef.setBookmarkName("MyAskField");
     builder.writeln();

     Assert.assertEquals(" REF  MyAskField", fieldRef.getFieldCode());

     // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
     FieldAsk fieldAsk = (FieldAsk) builder.insertField(FieldType.FIELD_ASK, true);
     fieldAsk.setBookmarkName("MyAskField");
     fieldAsk.setPromptText("Please provide a response for this ASK field");
     fieldAsk.setDefaultResponse("Response from within the field.");
     fieldAsk.setPromptOnceOnMailMerge(true);
     builder.writeln();

     Assert.assertEquals(
             " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
             fieldAsk.getFieldCode());

     // ASK fields apply the default response to their respective REF fields during a mail merge.
     DataTable table = new DataTable("My Table");
     table.getColumns().add("Column 1");
     table.getRows().add("Row 1");
     table.getRows().add("Row 2");

     FieldMergeField fieldMergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     fieldMergeField.setFieldName("Column 1");

     // We can modify or override the default response in our ASK fields with a custom prompt responder,
     // which will occur during a mail merge.
     doc.getFieldOptions().setUserPromptRespondent(new MyPromptRespondent());
     doc.getMailMerge().execute(table);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.ASK.docx");
 }

 /// 
 /// Prepends text to the default response of an ASK field during a mail merge.
 /// 
 private static class MyPromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response from MyPromptRespondent. " + defaultResponse;
     }
 }
 
```
## Methods

| Method | Description |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String) | When implemented, returns a response from the user on prompting. |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String}
```
public abstract String respond(String promptText, String defaultResponse)
```


When implemented, returns a response from the user on prompting. Your implementation should return  null  to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window).

 **Examples:** 

Shows how to create an ASK field, and set its properties.

```

 public void fieldAsk() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Place a field where the response to our ASK field will be placed.
     FieldRef fieldRef = (FieldRef) builder.insertField(FieldType.FIELD_REF, true);
     fieldRef.setBookmarkName("MyAskField");
     builder.writeln();

     Assert.assertEquals(" REF  MyAskField", fieldRef.getFieldCode());

     // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
     FieldAsk fieldAsk = (FieldAsk) builder.insertField(FieldType.FIELD_ASK, true);
     fieldAsk.setBookmarkName("MyAskField");
     fieldAsk.setPromptText("Please provide a response for this ASK field");
     fieldAsk.setDefaultResponse("Response from within the field.");
     fieldAsk.setPromptOnceOnMailMerge(true);
     builder.writeln();

     Assert.assertEquals(
             " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
             fieldAsk.getFieldCode());

     // ASK fields apply the default response to their respective REF fields during a mail merge.
     DataTable table = new DataTable("My Table");
     table.getColumns().add("Column 1");
     table.getRows().add("Row 1");
     table.getRows().add("Row 2");

     FieldMergeField fieldMergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     fieldMergeField.setFieldName("Column 1");

     // We can modify or override the default response in our ASK fields with a custom prompt responder,
     // which will occur during a mail merge.
     doc.getFieldOptions().setUserPromptRespondent(new MyPromptRespondent());
     doc.getMailMerge().execute(table);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.ASK.docx");
 }

 /// 
 /// Prepends text to the default response of an ASK field during a mail merge.
 /// 
 private static class MyPromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response from MyPromptRespondent. " + defaultResponse;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| promptText | java.lang.String | Prompt text (i.e. title of the prompt window). |
| defaultResponse | java.lang.String | Default user response (i.e. initial value contained in the prompt window). |

**Returns:**
java.lang.String - User response (i.e. confirmed value contained in the prompt window).
