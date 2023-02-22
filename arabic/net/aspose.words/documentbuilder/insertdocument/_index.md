---
title: DocumentBuilder.InsertDocument
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج مستند في موضع المؤشر .
type: docs
weight: 290
url: /ar/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(Document, ImportFormatMode) {#insertdocument}

إدراج مستند في موضع المؤشر .

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | وثيقة مصدر للإدراج. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |

### قيمة الإرجاع

العقدة الأولى للمحتوى المدرج.

### ملاحظات

تحاكي هذه الطريقة سلوك MS Word ، كما لو تم الضغط على CTRL + 'A' (حدد كل المحتوى) ، ثم CTRL + 'C' (تم تحديد النسخ في المخزن المؤقت) داخل مستند واحد_ ثم CTRL + 'V' (أدخل محتوى من المخزن المؤقت) داخل مستند آخر.

### أمثلة

يوضح كيفية إدراج مستند في مستند آخر.

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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertDocument(Document, ImportFormatMode, ImportFormatOptions) {#insertdocument_1}

إدراج مستند في موضع المؤشر .

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | وثيقة مصدر للإدراج. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |
| importFormatOptions | ImportFormatOptions | يسمح بتحديد الخيارات التي تؤثر على تنسيق الوثيقة الناتجة. |

### قيمة الإرجاع

العقدة الأولى للمحتوى المدرج.

### ملاحظات

تحاكي هذه الطريقة سلوك MS Word ، كما لو تم الضغط على CTRL + 'A' (حدد كل المحتوى) ، ثم CTRL + 'C' (تم تحديد النسخ في المخزن المؤقت) داخل مستند واحد_ ثم CTRL + 'V' (أدخل محتوى من المخزن المؤقت) داخل مستند آخر.

### أمثلة

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

// استنساخ المستند وتعديل نمط "MyStyle" الخاص بالنسخة ، بحيث يكون لونه مختلفًا عن اللون الأصلي.
// إذا أدخلنا النسخة في المستند الأصلي ، فإن النمطين اللذين يحملان الاسم نفسه سيتسببان في حدوث تضارب.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// عندما نقوم بتمكين SmartStyleBehavior واستخدام وضع تنسيق الاستيراد KeepSourceFormatting ،
// Aspose.Words سوف تحل تضارب الأنماط عن طريق تحويل أنماط الوثيقة المصدر.
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


