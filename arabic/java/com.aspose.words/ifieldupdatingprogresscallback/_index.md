---
title: "IFieldUpdatingProgressCallback"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا كنت ترغب في تتبع تقدم تحديث الحقول في Java."
type: docs
weight: 769
url: /ar/java/com.aspose.words/ifieldupdatingprogresscallback/
---
```
public interface IFieldUpdatingProgressCallback
```

قم بتنفيذ هذه الواجهة إذا كنت تريد تتبع تقدم تحديث الحقل.

 **Examples:** 

يوضح كيفية استخدام طرق الاستدعاء أثناء تحديث الحقل.

```

 public void fieldUpdatingCallbackTest() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");

     FieldUpdatingCallback callback = new FieldUpdatingCallback();
     doc.getFieldOptions().setFieldUpdatingCallback(callback);

     doc.updateFields();

     Assert.assertTrue(callback.getFieldUpdatedCalls().contains("Updating John Doe"));
 }

 /// 
 /// Implement this interface if you want to have your own custom methods called during a field update.
 /// 
 public static class FieldUpdatingCallback implements IFieldUpdatingCallback
 {
     public FieldUpdatingCallback()
     {
         mFieldUpdatedCalls = new ArrayList();
     }

     /// 
     /// A user defined method that is called just before a field is updated.
     /// 
     public void fieldUpdating(Field field) {
         if (field.getType() == FieldType.FIELD_AUTHOR)
         {
             FieldAuthor fieldAuthor = (FieldAuthor) field;
             try {
                 fieldAuthor.setAuthorName("Updating John Doe");
             } catch (Exception e) {
                 e.printStackTrace();
             }
         }
     }

     /// 
     /// A user defined method that is called just after a field is updated.
     /// 
     public void fieldUpdated(Field field)
     {
         getFieldUpdatedCalls().add(field.getResult());
     }

     public ArrayList getFieldUpdatedCalls() { return mFieldUpdatedCalls; };

     private ArrayList mFieldUpdatedCalls;
 }
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [notify(FieldUpdatingProgressArgs args)](#notify-com.aspose.words.FieldUpdatingProgressArgs) | طريقة معرفة من قبل المستخدم تُستدعى عندما يتغير تقدم التحديث. |
### notify(FieldUpdatingProgressArgs args) {#notify-com.aspose.words.FieldUpdatingProgressArgs}
```
public abstract void notify(FieldUpdatingProgressArgs args)
```


طريقة معرفة من قبل المستخدم تُستدعى عندما يتغير تقدم التحديث.

 **Examples:** 

يوضح كيفية استخدام طرق الاستدعاء أثناء تحديث الحقل.

```

 public void fieldUpdatingCallbackTest() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");

     FieldUpdatingCallback callback = new FieldUpdatingCallback();
     doc.getFieldOptions().setFieldUpdatingCallback(callback);

     doc.updateFields();

     Assert.assertTrue(callback.getFieldUpdatedCalls().contains("Updating John Doe"));
 }

 /// 
 /// Implement this interface if you want to have your own custom methods called during a field update.
 /// 
 public static class FieldUpdatingCallback implements IFieldUpdatingCallback
 {
     public FieldUpdatingCallback()
     {
         mFieldUpdatedCalls = new ArrayList();
     }

     /// 
     /// A user defined method that is called just before a field is updated.
     /// 
     public void fieldUpdating(Field field) {
         if (field.getType() == FieldType.FIELD_AUTHOR)
         {
             FieldAuthor fieldAuthor = (FieldAuthor) field;
             try {
                 fieldAuthor.setAuthorName("Updating John Doe");
             } catch (Exception e) {
                 e.printStackTrace();
             }
         }
     }

     /// 
     /// A user defined method that is called just after a field is updated.
     /// 
     public void fieldUpdated(Field field)
     {
         getFieldUpdatedCalls().add(field.getResult());
     }

     public ArrayList getFieldUpdatedCalls() { return mFieldUpdatedCalls; };

     private ArrayList mFieldUpdatedCalls;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| args | [FieldUpdatingProgressArgs](../../com.aspose.words/fieldupdatingprogressargs/) |  |

