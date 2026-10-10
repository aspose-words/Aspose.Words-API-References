---
title: "IFieldUpdatingProgressCallback"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Aspose.Words for Java"
description: "如果您想在 Java 中跟踪字段更新进度，请实现此接口。"
type: docs
weight: 769
url: /zh/java/com.aspose.words/ifieldupdatingprogresscallback/
---
```
public interface IFieldUpdatingProgressCallback
```

如果您想跟踪字段更新进度，请实现此接口。

 **Examples:** 

展示如何在字段更新期间使用回调方法。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [notify(FieldUpdatingProgressArgs args)](#notify-com.aspose.words.FieldUpdatingProgressArgs) | 当更新进度更改时调用的用户定义方法。 |
### notify(FieldUpdatingProgressArgs args) {#notify-com.aspose.words.FieldUpdatingProgressArgs}
```
public abstract void notify(FieldUpdatingProgressArgs args)
```


当更新进度更改时调用的用户定义方法。

 **Examples:** 

展示如何在字段更新期间使用回调方法。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| args | [FieldUpdatingProgressArgs](../../com.aspose.words/fieldupdatingprogressargs/) |  |

