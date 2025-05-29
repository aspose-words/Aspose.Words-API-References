---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words لـ .NET
description: قم بإدراج المستندات بسهولة باستخدام طريقة InsertDocumentInline في DocumentBuilder، مما يعمل على تحسين سير عملك وتجربة تحرير المستندات.
type: docs
weight: 320
url: /ar/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

يقوم بإدراج مستند مضمن في موضع المؤشر.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | وثيقة المصدر للإدراج. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |
| importFormatOptions | ImportFormatOptions | يسمح بتحديد الخيارات التي تؤثر على تنسيق المستند الناتج. |

### قيمة الإرجاع

العقدة الأولى للمحتوى المدرج.

## ملاحظات

تحاكي هذه الطريقة سلوك MS Word، كما لو تم الضغط على CTRL+'A' (تحديد كل المحتوى)، ثم CTRL+'C' (نسخ المحدد في المخزن المؤقت) داخل مستند واحد ثم CTRL+'V' (إدراج محتوى من المخزن المؤقت) داخل مستند آخر.

كفرق عن[`InsertDocument`](../insertdocument/) هذه الطريقة تنقل محتوى فقرة المستند الوجهة، التي سبقتها الفقرة الأصلية، إلى آخر فقرة من المستند الأصلي. هذا يعني إزالة فاصل الفقرة من آخر فقرة.

لاحظ أنه إذا لم تكن العقدة الأخيرة في المستند المصدر فقرة، فلن يتم فعل أي شيء.

## أمثلة

يوضح كيفية إدراج مستند مضمنًا عند موضع المؤشر.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// إنشاء مستند الوجهة.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

//إدراج مستند المصدر في السطر الوجهة.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### أنظر أيضا

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
