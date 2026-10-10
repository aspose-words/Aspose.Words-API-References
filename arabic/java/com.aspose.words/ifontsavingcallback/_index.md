---
title: "IFontSavingCallback"
linktitle: "IFontSavingCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا أردت تلقي الإشعارات والتحكم في طريقة حفظ Aspose.Words للخطوط عند تصدير مستند إلى صيغة HTML في Java."
type: docs
weight: 771
url: /ar/java/com.aspose.words/ifontsavingcallback/
---
```
public interface IFontSavingCallback
```

قم بتنفيذ هذه الواجهة إذا كنت تريد تلقي الإشعارات والتحكم في طريقة حفظ Aspose.Words للخطوط عند تصدير مستند إلى صيغة HTML.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fontSaving(FontSavingArgs args)](#fontSaving-com.aspose.words.FontSavingArgs) | يُستدعى عندما تكون Aspose.Words على وشك حفظ مورد الخط. |
### fontSaving(FontSavingArgs args) {#fontSaving-com.aspose.words.FontSavingArgs}
```
public abstract void fontSaving(FontSavingArgs args)
```


يُستدعى عندما تكون Aspose.Words على وشك حفظ مورد الخط.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| args | [FontSavingArgs](../../com.aspose.words/fontsavingargs/) |  |

