---
title: IFieldResultFormatter
linktitle: IFieldResultFormatter
second_title: Aspose.Words for Java
description: Implement this interface if you want to control how the field result is formatted in Java.
type: docs
weight: 762
url: /java/com.aspose.words/ifieldresultformatter/
---
```
public interface IFieldResultFormatter
```

Implement this interface if you want to control how the field result is formatted.

 **Examples:** 

Shows how to automatically apply a custom format to field results as the fields are updated.

```

 public void fieldResultFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldResultFormatter formatter = new FieldResultFormatter("$%d", "Date: %tb", "Item # %s:");
     doc.getFieldOptions().setResultFormatter(formatter);

     // Our field result formatter applies a custom format to newly created fields of three types of formats.
     // Field result formatters apply new formatting to fields as they are updated,
     // which happens as soon as we create them using this InsertField method overload.
     // 1 -  Numeric:
     builder.insertField(" = 2 + 3 \\# $###");

     Assert.assertEquals("$5", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.NUMERIC));

     // 2 -  Date/time:
     builder.insertField("DATE \\@ \"d MMMM yyyy\"");

     Assert.assertTrue(doc.getRange().getFields().get(1).getResult().startsWith("Date: "));
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.DATE_TIME));

     // 3 -  General:
     builder.insertField("QUOTE \"2\" \\* Ordinal");

     Assert.assertEquals("Item # 2:", doc.getRange().getFields().get(2).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.GENERAL));

     formatter.printFormatInvocations();
 }

 /// 
 /// When fields with formatting are updated, this formatter will override their formatting
 /// with a custom format, while tracking every invocation.
 /// 
 private static class FieldResultFormatter implements IFieldResultFormatter {
     public FieldResultFormatter(String numberFormat, String dateFormat, String generalFormat) {
         mNumberFormat = numberFormat;
         mDateFormat = dateFormat;
         mGeneralFormat = generalFormat;
     }

     public String formatNumeric(double value, String format) {
         if (mNumberFormat.isEmpty())
             return null;

         String newValue = String.format(mNumberFormat, (long) value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.NUMERIC, value, format, newValue));
         return newValue;
     }

     public String formatDateTime(Date value, String format, int calendarType) {
         if (mDateFormat.isEmpty())
             return null;

         String newValue = String.format(mDateFormat, value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.DATE_TIME, MessageFormat.format("{0} ({1})", value, calendarType), format, newValue));
         return newValue;
     }

     public String format(String value, int format) {
         return format((Object) value, format);
     }

     public String format(double value, int format) {
         return format((Object) value, format);
     }

     private String format(Object value, int format) {
         if (mGeneralFormat.isEmpty())
             return null;

         String newValue = String.format(mGeneralFormat, new DecimalFormat("#.###").format(value));
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.GENERAL, value, GeneralFormat.toString(format), newValue));
         return newValue;
     }

     public int countFormatInvocations(int formatInvocationType) {
         if (formatInvocationType == FormatInvocationType.ALL)
             return getFormatInvocations().size();

         return (int) IterableUtils.countMatches(getFormatInvocations(), i -> i.getFormatInvocationType() == formatInvocationType);
     }

     public void printFormatInvocations() {
         for (FormatInvocation f : getFormatInvocations())
             System.out.println(MessageFormat.format("Invocation type:\t{0}\n" +
                     "\tOriginal value:\t\t{1}\n" +
                     "\tOriginal format:\t{2}\n" +
                     "\tNew value:\t\t\t{3}\n", f.getFormatInvocationType(), f.getValue(), f.getOriginalFormat(), f.getNewValue()));
     }

     private final String mNumberFormat;
     private final String mDateFormat;
     private final String mGeneralFormat;

     private ArrayList getFormatInvocations() {
         return mFormatInvocations;
     }

     private final ArrayList mFormatInvocations = new ArrayList<>();

     private static class FormatInvocation {
         public int getFormatInvocationType() {
             return mFormatInvocationType;
         }

         private final int mFormatInvocationType;

         public Object getValue() {
             return mValue;
         }

         private final Object mValue;

         public String getOriginalFormat() {
             return mOriginalFormat;
         }

         private final String mOriginalFormat;

         public String getNewValue() {
             return mNewValue;
         }

         private final String mNewValue;

         public FormatInvocation(int formatInvocationType, Object value, String originalFormat, String newValue) {
             mValue = value;
             mFormatInvocationType = formatInvocationType;
             mOriginalFormat = originalFormat;
             mNewValue = newValue;
         }
     }

     public final class FormatInvocationType {
         private FormatInvocationType() {
         }

         public static final int NUMERIC = 0;
         public static final int DATE_TIME = 1;
         public static final int GENERAL = 2;
         public static final int ALL = 3;

         public static final int length = 4;
     }
 }
 
```
## Methods

| Method | Description |
| --- | --- |
| [format(double value, int format)](#format-double-int) |  |
| [format(String value, int format)](#format-java.lang.String-int) |  |
| [formatDateTime(Date value, String format, int calendarType)](#formatDateTime-java.util.Date-java.lang.String-int) |  |
| [formatNumeric(double value, String format)](#formatNumeric-double-java.lang.String) | Called when Aspose.Words applies a numeric format switch, i.e. |
### format(double value, int format) {#format-double-int}
```
public abstract String format(double value, int format)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |
| format | int |  |

**Returns:**
java.lang.String
### format(String value, int format) {#format-java.lang.String-int}
```
public abstract String format(String value, int format)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String |  |
| format | int |  |

**Returns:**
java.lang.String
### formatDateTime(Date value, String format, int calendarType) {#formatDateTime-java.util.Date-java.lang.String-int}
```
public abstract String formatDateTime(Date value, String format, int calendarType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date |  |
| format | java.lang.String |  |
| calendarType | int |  |

**Returns:**
java.lang.String
### formatNumeric(double value, String format) {#formatNumeric-double-java.lang.String}
```
public abstract String formatNumeric(double value, String format)
```


Called when Aspose.Words applies a numeric format switch, i.e. \\\# "\#.\#".

 **Remarks:** 

The implementation should return  null  to indicate that the default formatting should be applied.

 **Examples:** 

Shows how to automatically apply a custom format to field results as the fields are updated.

```

 public void fieldResultFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldResultFormatter formatter = new FieldResultFormatter("$%d", "Date: %tb", "Item # %s:");
     doc.getFieldOptions().setResultFormatter(formatter);

     // Our field result formatter applies a custom format to newly created fields of three types of formats.
     // Field result formatters apply new formatting to fields as they are updated,
     // which happens as soon as we create them using this InsertField method overload.
     // 1 -  Numeric:
     builder.insertField(" = 2 + 3 \\# $###");

     Assert.assertEquals("$5", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.NUMERIC));

     // 2 -  Date/time:
     builder.insertField("DATE \\@ \"d MMMM yyyy\"");

     Assert.assertTrue(doc.getRange().getFields().get(1).getResult().startsWith("Date: "));
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.DATE_TIME));

     // 3 -  General:
     builder.insertField("QUOTE \"2\" \\* Ordinal");

     Assert.assertEquals("Item # 2:", doc.getRange().getFields().get(2).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.GENERAL));

     formatter.printFormatInvocations();
 }

 /// 
 /// When fields with formatting are updated, this formatter will override their formatting
 /// with a custom format, while tracking every invocation.
 /// 
 private static class FieldResultFormatter implements IFieldResultFormatter {
     public FieldResultFormatter(String numberFormat, String dateFormat, String generalFormat) {
         mNumberFormat = numberFormat;
         mDateFormat = dateFormat;
         mGeneralFormat = generalFormat;
     }

     public String formatNumeric(double value, String format) {
         if (mNumberFormat.isEmpty())
             return null;

         String newValue = String.format(mNumberFormat, (long) value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.NUMERIC, value, format, newValue));
         return newValue;
     }

     public String formatDateTime(Date value, String format, int calendarType) {
         if (mDateFormat.isEmpty())
             return null;

         String newValue = String.format(mDateFormat, value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.DATE_TIME, MessageFormat.format("{0} ({1})", value, calendarType), format, newValue));
         return newValue;
     }

     public String format(String value, int format) {
         return format((Object) value, format);
     }

     public String format(double value, int format) {
         return format((Object) value, format);
     }

     private String format(Object value, int format) {
         if (mGeneralFormat.isEmpty())
             return null;

         String newValue = String.format(mGeneralFormat, new DecimalFormat("#.###").format(value));
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.GENERAL, value, GeneralFormat.toString(format), newValue));
         return newValue;
     }

     public int countFormatInvocations(int formatInvocationType) {
         if (formatInvocationType == FormatInvocationType.ALL)
             return getFormatInvocations().size();

         return (int) IterableUtils.countMatches(getFormatInvocations(), i -> i.getFormatInvocationType() == formatInvocationType);
     }

     public void printFormatInvocations() {
         for (FormatInvocation f : getFormatInvocations())
             System.out.println(MessageFormat.format("Invocation type:\t{0}\n" +
                     "\tOriginal value:\t\t{1}\n" +
                     "\tOriginal format:\t{2}\n" +
                     "\tNew value:\t\t\t{3}\n", f.getFormatInvocationType(), f.getValue(), f.getOriginalFormat(), f.getNewValue()));
     }

     private final String mNumberFormat;
     private final String mDateFormat;
     private final String mGeneralFormat;

     private ArrayList getFormatInvocations() {
         return mFormatInvocations;
     }

     private final ArrayList mFormatInvocations = new ArrayList<>();

     private static class FormatInvocation {
         public int getFormatInvocationType() {
             return mFormatInvocationType;
         }

         private final int mFormatInvocationType;

         public Object getValue() {
             return mValue;
         }

         private final Object mValue;

         public String getOriginalFormat() {
             return mOriginalFormat;
         }

         private final String mOriginalFormat;

         public String getNewValue() {
             return mNewValue;
         }

         private final String mNewValue;

         public FormatInvocation(int formatInvocationType, Object value, String originalFormat, String newValue) {
             mValue = value;
             mFormatInvocationType = formatInvocationType;
             mOriginalFormat = originalFormat;
             mNewValue = newValue;
         }
     }

     public final class FormatInvocationType {
         private FormatInvocationType() {
         }

         public static final int NUMERIC = 0;
         public static final int DATE_TIME = 1;
         public static final int GENERAL = 2;
         public static final int ALL = 3;

         public static final int length = 4;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |
| format | java.lang.String |  |

**Returns:**
java.lang.String
