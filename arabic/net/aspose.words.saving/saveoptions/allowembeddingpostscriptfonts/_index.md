---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words لـ .NET
description: SaveOptions AllowEmbeddingPostScriptFonts ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم السماح بدمج الخطوط باستخدام مخططات PostScript عند حفظ تضمين خطوط TrueType في مستند. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم السماح بدمج الخطوط باستخدام مخططات PostScript عند حفظ تضمين خطوط TrueType في مستند. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## ملاحظات

لاحظ أن Word لا يقوم بتضمين خطوط PostScript، لكن يمكنه فتح مستندات تحتوي على خطوط مضمنة من هذا النوع.

هذا الخيار يعمل فقط عندما[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) من the [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) تم تعيين الخاصية على`حقيقي`.

## أمثلة

يوضح كيفية حفظ المستند بخط PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// قم بتحميل الخط باستخدام PostScript لاستخدامه في المستند.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// تضمين خطوط تروتايب.
doc.FontInfos.EmbedTrueTypeFonts = true;

// السماح بتضمين خطوط PostScript أثناء تضمين خطوط TrueType.
// لا يقوم Microsoft Word بتضمين خطوط PostScript، لكن يمكنه فتح مستندات تحتوي على خطوط مضمنة من هذا النوع.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
