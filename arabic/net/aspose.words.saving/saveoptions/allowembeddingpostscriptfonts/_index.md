---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words لـ .NET
description: تحكم بتضمين الخطوط في مستنداتك باستخدام AllowEmbeddingPostScriptFonts من SaveOptions. أدر خيارات خطوط TrueType بسهولة لتحسين جودة مستنداتك.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم السماح بتضمين الخطوط مع الخطوط العريضة لـ PostScript عند تضمين خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## ملاحظات

لاحظ أن Word لا يقوم بتضمين خطوط PostScript، ولكن يمكنه فتح المستندات التي تحتوي على خطوط مضمنة من هذا النوع.

هذا الخيار يعمل فقط عندما[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) من [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) تم تعيين الخاصية إلى`حقيقي`.

## أمثلة

يوضح كيفية حفظ المستند باستخدام خط PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// قم بتحميل الخط باستخدام PostScript لاستخدامه في المستند.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// تضمين خطوط TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

//السماح بتضمين خطوط PostScript أثناء تضمين خطوط TrueType.
// لا يقوم Microsoft Word بتضمين خطوط PostScript، ولكن يمكنه فتح المستندات التي تحتوي على خطوط مضمنة من هذا النوع.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
