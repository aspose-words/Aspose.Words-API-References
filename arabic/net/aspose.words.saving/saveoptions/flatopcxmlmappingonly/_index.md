---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيينXmlMapping . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### ملاحظات

تم إقران هذا الخيار مع[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . عادةً ما تحتاج إلى تعيين كلاهما على خطأ للسماح بتعيين تنسيق مستند تعسفي.

### أمثلة

يوضح كيفية ربط علامات المستند المهيكلة بأي تنسيق.

```csharp
// إذا كان هذا صحيحًا - ستحتوي SDT على نص HTML خام.
// إذا كان خطأ - سيتم تحليل HTML المعين وسيتم إدراج المستند الناتج في محتوى SDT.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


