---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: Aspose.Words لـ .NET
description: قم بالتنقل بسهولة عبر مستندك باستخدام طريقة MoveToCell في DocumentBuilder، مما يؤدي إلى وضع المؤشر بسرعة في أي خلية في الجدول لتحسين التحرير.
type: docs
weight: 540
url: /ar/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

يحرك المؤشر إلى خلية الجدول في القسم الحالي.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableIndex | Int32 | فهرس الجدول الذي سيتم الانتقال إليه. |
| rowIndex | Int32 | مؤشر الصف في الجدول. |
| columnIndex | Int32 | فهرس العمود في الجدول. |
| characterIndex | Int32 | مؤشر الحرف داخل الخلية. . تسمح لك القيمة السالبة بتحديد موضع من نهاية الخلية. استخدم -1 للانتقال إلى نهاية الخلية. |

## ملاحظات

يتم التنقل داخل القصة الحالية للقسم الحالي.

بالنسبة لمعلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، يُحدد فهرس from في البداية، حيث يكون 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، يُحدد فهرس from في النهاية، حيث يكون -1 هو العنصر الأخير.

## أمثلة

يوضح كيفية نقل مؤشر منشئ المستندات إلى خلية في جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء جدول فارغ 2x2.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// لأننا أنهينا الجدول بطريقة EndTable،
// مؤشر منشئ المستند موجود حاليًا خارج الجدول.
// يتمتع هذا المؤشر بنفس وظيفة مؤشر النص الوامض في برنامج Microsoft Word.
//يمكن أيضًا نقله إلى موقع مختلف في المستند باستخدام طرق MoveTo الخاصة بالمنشئ.
//يمكننا نقل المؤشر مرة أخرى داخل الجدول إلى خلية محددة.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
