---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: Aspose.Words لـ .NET
description: أدرج المستندات بسهولة في أي موضع مؤشر باستخدام طريقة InsertDocument من DocumentBuilder. بسّط سير عملك وحسّن إنتاجيتك!
type: docs
weight: 310
url: /ar/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

إدراج مستند في موضع المؤشر.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | وثيقة المصدر للإدراج. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |

### قيمة الإرجاع

العقدة الأولى للمحتوى المدرج.

## ملاحظات

تحاكي هذه الطريقة سلوك MS Word، كما لو تم الضغط على CTRL+'A' (تحديد كل المحتوى)، ثم CTRL+'C' (نسخ المحدد في المخزن المؤقت) داخل مستند واحد ثم CTRL+'V' (إدراج محتوى من المخزن المؤقت) داخل مستند آخر.

## أمثلة

يوضح كيفية إدراج مستند داخل مستند آخر.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### أنظر أيضا

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

إدراج مستند في موضع المؤشر.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
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

## أمثلة

يوضح كيفية حل الأنماط المكررة أثناء إدراج المستندات.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// استنساخ المستند وتحرير نمط "MyStyle" الخاص بالاستنساخ، بحيث يكون لونه مختلفًا عن اللون الأصلي.
// إذا قمنا بإدراج النسخة المستنسخة في المستند الأصلي، فإن النمطين اللذين يحملان نفس الاسم سوف يتسببان في حدوث تعارض.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// عندما نقوم بتمكين SmartStyleBehavior واستخدام وضع تنسيق الاستيراد KeepSourceFormatting،
// سيقوم Aspose.Words بحل تضارب الأنماط عن طريق تحويل أنماط المستند المصدر.
// بنفس أسماء أنماط الوجهة في سمات الفقرة المباشرة.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### أنظر أيضا

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
