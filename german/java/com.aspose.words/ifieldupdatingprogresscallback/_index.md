---
title: "IFieldUpdatingProgressCallback"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie den Fortschritt der Feldaktualisierung in Java verfolgen möchten."
type: docs
weight: 769
url: /de/java/com.aspose.words/ifieldupdatingprogresscallback/
---
```
public interface IFieldUpdatingProgressCallback
```

Implementieren Sie dieses Interface, wenn Sie den Fortschritt der Feldaktualisierung verfolgen möchten.

 **Examples:** 

Zeigt, wie Callback-Methoden während einer Feldaktualisierung verwendet werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [notify(FieldUpdatingProgressArgs args)](#notify-com.aspose.words.FieldUpdatingProgressArgs) | Eine benutzerdefinierte Methode, die aufgerufen wird, wenn sich der Aktualisierungsfortschritt ändert. |
### notify(FieldUpdatingProgressArgs args) {#notify-com.aspose.words.FieldUpdatingProgressArgs}
```
public abstract void notify(FieldUpdatingProgressArgs args)
```


Eine benutzerdefinierte Methode, die aufgerufen wird, wenn sich der Aktualisierungsfortschritt ändert.

 **Examples:** 

Zeigt, wie Callback-Methoden während einer Feldaktualisierung verwendet werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [FieldUpdatingProgressArgs](../../com.aspose.words/fieldupdatingprogressargs/) |  |

