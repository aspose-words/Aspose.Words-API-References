---
title: PageSetup.BorderSurroundsFooter
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. تحديد ما إذا كان حد الصفحة يتضمن التذييل أو يستبعده.
type: docs
weight: 60
url: /ar/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

تحديد ما إذا كان حد الصفحة يتضمن التذييل أو يستبعده.

```csharp
public bool BorderSurroundsFooter { get; set; }
```

### ملاحظات

ملاحظة ، يؤثر تغيير هذه الخاصية على جميع أقسام المستند.

### أمثلة

يوضح كيفية تطبيق حد على الصفحة والرأس / التذييل.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// أدخل حد خط مزدوج أزرق.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// يحتوي كائن PageSetup لقسم على علامتي "BorderSurroundsHeader" و "BorderSurroundsFooter" التي تحدد
// ما إذا كان حد الصفحة يحيط بالنص الأساسي ، يتضمن أيضًا الرأس أو التذييل ، على التوالي.
// اضبط علامة "BorderSurroundsHeader" على "true" لإحاطة الرأس بحدودنا ،
// ثم قم بتعيين علامة "BorderSurroundsFooter" لترك التذييل خارج الحدود.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


