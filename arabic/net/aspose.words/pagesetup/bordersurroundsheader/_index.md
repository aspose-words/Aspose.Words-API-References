---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup BorderSurroundsHeader لتخصيص حدود صفحتك. تحكم في تضمين الرأس للحصول على تصميم أنيق للمستند.
type: docs
weight: 70
url: /ar/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

يحدد ما إذا كانت حدود الصفحة تتضمن الرأس أم تستبعده.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## ملاحظات

ملاحظة: تغيير هذه الخاصية يؤثر على جميع الأقسام في المستند.

## أمثلة

يوضح كيفية تطبيق حدود على الصفحة والرأس/التذييل.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

//أدرج حدودًا مزدوجة الخطوط باللون الأزرق.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// يحتوي كائن PageSetup الخاص بالقسم على علامتي "BorderSurroundsHeader" و"BorderSurroundsFooter" اللتين تحددان
// ما إذا كان إطار الصفحة يحيط بنص الهيئة الرئيسي، ويتضمن أيضًا الرأس أو التذييل، على التوالي.
// اضبط علامة "BorderSurroundsHeader" على "true" لإحاطة الرأس بحدودنا،
// ثم قم بتعيين العلم "BorderSurroundsFooter" لترك التذييل خارج الحدود.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
