---
title: "IHyphenationCallback"
linktitle: "IHyphenationCallback"
second_title: "Aspose.Words لـ Java"
description: "يتم تنفيذها بواسطة الفئات التي يمكنها تسجيل قواميس التجزئة في Java."
type: docs
weight: 772
url: /ar/java/com.aspose.words/ihyphenationcallback/
---
```
public interface IHyphenationCallback
```

يتم تنفيذها بواسطة الفئات التي يمكنها تسجيل قواميس التجزئة.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [requestDictionary(String language)](#requestDictionary-java.lang.String) | يُخطر التطبيق بأن قاموس التجزئة للغة المحددة لم يُعثر عليه وقد يحتاج إلى التسجيل. |
### requestDictionary(String language) {#requestDictionary-java.lang.String}
```
public abstract void requestDictionary(String language)
```


يُخطر التطبيق بأن قاموس التجزئة للغة المحددة لم يُعثر عليه وقد يحتاج إلى التسجيل.

يجب على التنفيذ العثور على قاموس وتسجيله باستخدام طرق **M:Aspose.Words.Hyphenation.RegisterDictionary(System.String,System.IO.Stream)**.

إذا كان القاموس غير متوفر للغة المحددة، يمكن للتنفيذ إلغاء المزيد من الاستدعاءات لنفس اللغة باستخدام [Hyphenation.registerDictionary(java.lang.String, java.lang.String)](../../com.aspose.words/hyphenation/\#registerDictionary-java.lang.String--java.lang.String) بقيمة  null .

 **Remarks:** 

ستؤدي الاستثناءات التي تُرمى من هذه الطريقة إلى إيقاف تنفيذ عملية تخطيط الصفحة.

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
| اللغة | java.lang.String | اسم لغة، مثل "en-US". راجع وثائق .NET لـ "culture name" وRFC 4646 للحصول على التفاصيل. |

