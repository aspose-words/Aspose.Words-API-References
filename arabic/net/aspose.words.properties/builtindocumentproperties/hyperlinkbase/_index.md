---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words لـ .NET
description: BuiltInDocumentProperties HyperlinkBase ملكية. يحدد السلسلة الأساسية المستخدمة لتقييم الارتباطات التشعبية النسبية في هذا المستند في C#.
type: docs
weight: 120
url: /ar/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

يحدد السلسلة الأساسية المستخدمة لتقييم الارتباطات التشعبية النسبية في هذا المستند.

```csharp
public string HyperlinkBase { get; set; }
```

## ملاحظات

Aspose.Words لا يستخدم هذه الخاصية.

## أمثلة

يوضح كيفية تخزين الجزء الأساسي من الارتباط التشعبي في خصائص المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج ارتباط تشعبي نسبي لمستند في نظام الملفات المحلي المسمى "Document.docx".
// سيؤدي النقر فوق الارتباط في Microsoft Word إلى فتح المستند المحدد، إذا كان متاحًا.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// هذا الرابط نسبي. إذا لم يكن هناك "Document.docx" في نفس المجلد
// باعتباره المستند الذي يحتوي على هذا الرابط، سيتم قطع الرابط.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// المستند الذي نحاول الارتباط به موجود في دليل مختلف عن الدليل الذي نخطط لحفظ المستند فيه.
 // يمكننا إصلاح روابط مثل هذه عن طريق وضع اسم ملف مطلق في كل رابط.
// بدلاً من ذلك، يمكننا توفير رابط أساسي لكل رابط تشعبي باسم ملف نسبي
 // سيضاف إلى الرابط الخاص به عندما نضغط عليه.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
