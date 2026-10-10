---
title: "IFieldUpdatingCallback"
linktitle: "IFieldUpdatingCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا كنت ترغب في وجود طرق مخصصة خاصة بك تُستدعى أثناء تحديث الحقل في Java."
type: docs
weight: 768
url: /ar/java/com.aspose.words/ifieldupdatingcallback/
---
```
public interface IFieldUpdatingCallback
```

قم بتنفيذ هذه الواجهة إذا كنت ترغب في استدعاء طرقك المخصصة الخاصة أثناء تحديث الحقل.

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
| [fieldUpdated(Field field)](#fieldUpdated-com.aspose.words.Field) | طريقة معرفة من قبل المستخدم تُستدعى مباشرةً بعد تحديث الحقل. |
| [fieldUpdating(Field field)](#fieldUpdating-com.aspose.words.Field) | طريقة معرفة من قبل المستخدم تُستدعى مباشرةً قبل تحديث الحقل. |
### fieldUpdated(Field field) {#fieldUpdated-com.aspose.words.Field}
```
public abstract void fieldUpdated(Field field)
```


طريقة معرفة من قبل المستخدم تُستدعى مباشرةً بعد تحديث الحقل.

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
| field | [Field](../../com.aspose.words/field/) |  |

### fieldUpdating(Field field) {#fieldUpdating-com.aspose.words.Field}
```
public abstract void fieldUpdating(Field field)
```


طريقة معرفة من قبل المستخدم تُستدعى مباشرةً قبل تحديث الحقل.

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
| field | [Field](../../com.aspose.words/field/) |  |

