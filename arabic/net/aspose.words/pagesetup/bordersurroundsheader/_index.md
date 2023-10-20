---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words لـ .NET
description: PageSetup BorderSurroundsHeader ملكية. يحدد ما إذا كانت حدود الصفحة تتضمن الرأس أم لا في C#.
type: docs
weight: 70
url: /ar/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

يحدد ما إذا كانت حدود الصفحة تتضمن الرأس أم لا.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## ملاحظات

لاحظ أن تغيير هذه الخاصية يؤثر على كافة الأقسام في المستند.

## أمثلة

يوضح كيفية تطبيق حد على الصفحة والرأس/التذييل.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// أدخل حدًا أزرقًا مزدوج الخط.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// يحتوي كائن PageSetup الخاص بالقسم على علامتي "BorderSurroundsHeader" و"BorderSurroundsFooter" التي تحدد
// ما إذا كان حد الصفحة يحيط بالنص الأساسي، أم لا، ويتضمن أيضًا الرأس أو التذييل، على التوالي.
// اضبط علامة "BorderSurroundsHeader" على "صحيح" لإحاطة الرأس بحدودنا،
// ثم قم بتعيين علامة "BorderSurroundsFooter" لترك التذييل خارج الحدود.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
