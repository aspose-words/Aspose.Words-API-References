---
title: DocumentSavingArgs
linktitle: DocumentSavingArgs
second_title: Aspose.Words for Java
description: An argument passed into IDocumentSavingCallback.notifycom.aspose.words.DocumentSavingArgs in Java.
type: docs
weight: 158
url: /java/com.aspose.words/documentsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSavingArgs
```

An argument passed into [IDocumentSavingCallback.notify(com.aspose.words.DocumentSavingArgs)](../../com.aspose.words/idocumentsavingcallback/\#notify-com.aspose.words.DocumentSavingArgs).

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

 **Examples:** 

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [getEstimatedProgress()](#getEstimatedProgress) | Overall estimated percentage progress. |
### getEstimatedProgress() {#getEstimatedProgress}
```
public double getEstimatedProgress()
```


Overall estimated percentage progress.

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Returns:**
double - The corresponding  double  value.
