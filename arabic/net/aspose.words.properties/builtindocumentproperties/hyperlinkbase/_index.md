---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HyperlinkBase الخاصة بـ BuiltInDocumentProperties لتحسين الارتباطات التشعبية النسبية في مستنداتك لتحقيق تنقل سلس وتجربة مستخدم محسنة.
type: docs
weight: 120
url: /ar/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

يحدد السلسلة الأساسية المستخدمة لتقييم الارتباطات التشعبية النسبية في هذه الوثيقة.

```csharp
public string HyperlinkBase { get; set; }
```

## ملاحظات

لا يستخدم Aspose.Words هذه الخاصية.

## أمثلة

يوضح كيفية تخزين الجزء الأساسي من ارتباط تشعبي في خصائص المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج ارتباط تشعبي نسبي إلى مستند في نظام الملفات المحلي المسمى "Document.docx".
// الضغط على الرابط في Microsoft Word سوف يفتح المستند المحدد، إذا كان متاحا.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// هذا الرابط نسبي. إذا لم يكن هناك ملف "Document.docx" في نفس المجلد
// حيث أن المستند الذي يحتوي على هذا الرابط، سيكون الرابط معطلاً.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// المستند الذي نحاول الارتباط به موجود في دليل مختلف عن الدليل الذي نخطط لحفظ المستند فيه.
 // يمكننا إصلاح الروابط مثل هذا عن طريق وضع اسم ملف مطلق في كل منها.
// بدلاً من ذلك، يمكننا توفير رابط أساسي بحيث يكون لكل رابط تشعبي اسم ملف نسبي
 //سيتم إضافته إلى الرابط الخاص به عندما نضغط عليه.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
