---
title: "تقسيم الكلمات"
linktitle: "تقسيم الكلمات"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا للعمل مع قواميس تقسيم الكلمات في جافا."
type: docs
weight: 387
url: /ar/java/com.aspose.words/hyphenation/
---

**Inheritance:**
java.lang.Object
```
public class Hyphenation
```

يوفر طرقًا للعمل مع قواميس تقسيم الكلمات. هذه القواميس تحدد أين يمكن تقسيم كلمات لغة معينة.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Hyphenation ][Working with Hyphenation] .

 **Examples:** 

يوضح كيفية فتح وتسجيل قاموس من ملف.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCallback()](#getCallback) | يحصل على واجهة الاستدعاء المستخدمة لطلب القواميس عندما يتم بناء تخطيط صفحات المستند. |
| [getWarningCallback()](#getWarningCallback) | يُستدعى أثناء تحميل أنماط تقسيم الكلمات، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String) | يرجع  false  إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل فارغًا (Null)، ويرجع  true  غير ذلك. |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String) | يسجل ويحمل قاموس تجزئة الكلمات للغة المحددة من ملف. |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback) | يضبط واجهة الاستدعاء المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | يُستدعى أثناء تحميل أنماط تقسيم الكلمات، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String) | يلغي تسجيل قاموس تجزئة الكلمات للغة المحددة. |
### getCallback() {#getCallback}
```
public static IHyphenationCallback getCallback()
```


يحصل على واجهة الاستدعاء المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند. يتيح ذلك تحميل القواميس بتأخير قد يكون مفيدًا عند معالجة المستندات بعدة لغات.

 **Examples:** 

يوضح كيفية فتح وتسجيل قاموس من ملف.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Returns:**
[IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) - Callback interface used to request dictionaries when page layout of the document is built.
### getWarningCallback() {#getWarningCallback}
```
public static IWarningCallback getWarningCallback()
```


يُستدعى أثناء تحميل أنماط تقسيم الكلمات، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.

 **Examples:** 

يوضح كيفية فتح وتسجيل قاموس من ملف.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### isDictionaryRegistered(String language) {#isDictionaryRegistered-java.lang.String}
```
public static boolean isDictionaryRegistered(String language)
```


يرجع  false  إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل فارغًا (Null)، ويرجع  true  غير ذلك.

 **Examples:** 

يوضح كيفية تسجيل قاموس تجزئة الكلمات.

```

 // A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
 // When a document contains lines of text in which a word could be split up and continued on the next line,
 // hyphenation will look through the dictionary's list of strings for that word's substrings.
 // If the dictionary contains a substring, then hyphenation will split the word across two lines
 // by the substring and add a hyphen to the first half.
 // Register a dictionary file from the local file system to the "de-CH" locale.
 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary,
 // and save it to a fixed-page save format. The text in that document will be hyphenated.
 Document doc = new Document(getMyDir() + "German text.docx");

 Assert.assertTrue(IterableUtils.matchesAll(doc.getFirstSection().getBody().getFirstParagraph().getRuns(), r -> r.getFont().getLocaleId() == 2055));

 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Registered.pdf");

 // Re-load the document after un-registering the dictionary,
 // and save it to another PDF, which will not have hyphenated text.
 Hyphenation.unregisterDictionary("de-CH");

 Assert.assertFalse(Hyphenation.isDictionaryRegistered("de-CH"));

 doc = new Document(getMyDir() + "German text.docx");
 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Unregistered.pdf");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| اللغة | java.lang.String |  |

**Returns:**
boolean
### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream}
```
public static void registerDictionary(String language, InputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| اللغة | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String}
```
public static void registerDictionary(String language, String fileName)
```


يسجل ويحمل قاموس تجزئة الكلمات للغة المحددة من ملف. يطرح استثناء إذا تعذر قراءة القاموس أو كان بتنسيق غير صالح.

يمكن أيضًا استخدام هذه الطريقة لتسجيل قاموس Null لمنع [getCallback()](../../com.aspose.words/hyphenation/\#getCallback) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation/\#setCallback-com.aspose.words.IHyphenationCallback) من الاستدعاء المتكرر لنفس اللغة.

 **Examples:** 

يوضح كيفية تسجيل قاموس تجزئة الكلمات.

```

 // A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
 // When a document contains lines of text in which a word could be split up and continued on the next line,
 // hyphenation will look through the dictionary's list of strings for that word's substrings.
 // If the dictionary contains a substring, then hyphenation will split the word across two lines
 // by the substring and add a hyphen to the first half.
 // Register a dictionary file from the local file system to the "de-CH" locale.
 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary,
 // and save it to a fixed-page save format. The text in that document will be hyphenated.
 Document doc = new Document(getMyDir() + "German text.docx");

 Assert.assertTrue(IterableUtils.matchesAll(doc.getFirstSection().getBody().getFirstParagraph().getRuns(), r -> r.getFont().getLocaleId() == 2055));

 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Registered.pdf");

 // Re-load the document after un-registering the dictionary,
 // and save it to another PDF, which will not have hyphenated text.
 Hyphenation.unregisterDictionary("de-CH");

 Assert.assertFalse(Hyphenation.isDictionaryRegistered("de-CH"));

 doc = new Document(getMyDir() + "German text.docx");
 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Unregistered.pdf");
 
```

يوضح كيفية فتح وتسجيل قاموس من ملف.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| اللغة | java.lang.String | اسم لغة، مثل "en-US". راجع وثائق .NET لـ "culture name" وRFC 4646 للحصول على التفاصيل. |
|  | fileName | java.lang.String | مسار ملف القاموس بتنسيق Open Office. |

إذا كان هذا المعامل  null  أو سلسلة فارغة، فسيتم تسجيل قاموس Null ولن يتم استدعاء الواجهة مرة أخرى لهذه اللغة.

لتمكين الاستدعاء مرة أخرى استخدم طريقة [unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation/\#unregisterDictionary-java.lang.String). |

### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback}
```
public static void setCallback(IHyphenationCallback value)
```


يضبط واجهة الاستدعاء المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند. يتيح ذلك تحميل القواميس بتأخير قد يكون مفيدًا عند معالجة المستندات بعدة لغات.

 **Examples:** 

يوضح كيفية فتح وتسجيل قاموس من ملف.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) | واجهة الاستدعاء المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public static void setWarningCallback(IWarningCallback value)
```


يُستدعى أثناء تحميل أنماط تقسيم الكلمات، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.

 **Examples:** 

يوضح كيفية فتح وتسجيل قاموس من ملف.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String}
```
public static void unregisterDictionary(String language)
```


يلغي تسجيل قاموس تجزئة الكلمات للغة المحددة.

هذا مختلف عن تسجيل قاموس Null. إلغاء تسجيل القاموس يتيح الاستدعاء للغة المحددة.

 **Examples:** 

يوضح كيفية تسجيل قاموس تجزئة الكلمات.

```

 // A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
 // When a document contains lines of text in which a word could be split up and continued on the next line,
 // hyphenation will look through the dictionary's list of strings for that word's substrings.
 // If the dictionary contains a substring, then hyphenation will split the word across two lines
 // by the substring and add a hyphen to the first half.
 // Register a dictionary file from the local file system to the "de-CH" locale.
 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary,
 // and save it to a fixed-page save format. The text in that document will be hyphenated.
 Document doc = new Document(getMyDir() + "German text.docx");

 Assert.assertTrue(IterableUtils.matchesAll(doc.getFirstSection().getBody().getFirstParagraph().getRuns(), r -> r.getFont().getLocaleId() == 2055));

 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Registered.pdf");

 // Re-load the document after un-registering the dictionary,
 // and save it to another PDF, which will not have hyphenated text.
 Hyphenation.unregisterDictionary("de-CH");

 Assert.assertFalse(Hyphenation.isDictionaryRegistered("de-CH"));

 doc = new Document(getMyDir() + "German text.docx");
 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Unregistered.pdf");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
|  | اللغة | java.lang.String | اسم لغة، مثل "en-US". راجع وثائق .NET لـ "culture name" وRFC 4646 للحصول على التفاصيل. |

إذا كان  null  أو سلسلة فارغة فسيتم إلغاء تسجيل جميع القواميس. |

