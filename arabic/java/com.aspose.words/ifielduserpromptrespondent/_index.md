---
title: "IFieldUserPromptRespondent"
linktitle: "IFieldUserPromptRespondent"
second_title: "Aspose.Words لـ Java"
description: "يمثل المستجيب لمطالبات المستخدم أثناء تحديث الحقل في Java."
type: docs
weight: 770
url: /ar/java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface IFieldUserPromptRespondent
```

يمثل المستجيب لمطالبات المستخدم أثناء تحديث الحقل.

 **Remarks:** 

حقول ASK و FILLIN هي أمثلة على الحقول التي تطلب من المستخدم استجابة ما. نفّذ هذه الواجهة وعيّنها إلى خاصية [FieldOptions.getUserPromptRespondent()](../../com.aspose.words/fieldoptions/\#getUserPromptRespondent) / [FieldOptions.setUserPromptRespondent(com.aspose.words.IFieldUserPromptRespondent)](../../com.aspose.words/fieldoptions/\#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent) لتأسيس التفاعل بين تحديث الحقل والمستخدم.

 **Examples:** 

يوضح كيفية إنشاء حقل ASK، وتعيين خصائصه.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String) | عند التنفيذ، تُرجع استجابة من المستخدم عند الطلب. |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String}
```
public abstract String respond(String promptText, String defaultResponse)
```


عند التنفيذ، تُرجع استجابة من المستخدم عند الطلب. يجب على تنفيذك إرجاع  null  للإشارة إلى أن المستخدم لم يرد على الطلب (أي أن المستخدم ضغط زر إلغاء في نافذة الطلب).

 **Examples:** 

يوضح كيفية إنشاء حقل ASK، وتعيين خصائصه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| promptText | java.lang.String | نص الطلب (أي عنوان نافذة الطلب). |
| defaultResponse | java.lang.String | استجابة المستخدم الافتراضية (أي القيمة الأولية الموجودة في نافذة الطلب). |

**Returns:**
java.lang.String - استجابة المستخدم (أي القيمة المؤكدة الموجودة في نافذة الطلب).
