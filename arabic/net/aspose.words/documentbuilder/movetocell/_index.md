---
title: DocumentBuilder.MoveToCell
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. ينقل المؤشر إلى خلية جدول في القسم الحالي.
type: docs
weight: 480
url: /ar/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

ينقل المؤشر إلى خلية جدول في القسم الحالي.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tableIndex | Int32 | فهرس الجدول المراد الانتقال إليه. |
| rowIndex | Int32 | فهرس الصف في الجدول. |
| columnIndex | Int32 | فهرس العمود في الجدول. |
| characterIndex | Int32 | فهرس الحرف داخل الخلية . تسمح لك القيمة السالبة بتحديد موضع من نهاية الخلية. استخدم -1 للانتقال إلى نهاية الخلية. |

### ملاحظات

يتم التنقل داخل القصة الحالية للقسم الحالي.

بالنسبة لمعلمات الفهرس ، عندما يكون الفهرس أكبر من أو يساوي 0 ، فإنه يحدد فهرسًا من البداية مع كون 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0 ، فإنه يحدد فهرس from النهاية بحيث يكون -1 هو العنصر الأخير.

### أمثلة

يوضح كيفية نقل مؤشر منشئ المستندات إلى خلية في جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء جدول 2x2 فارغ.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// لأننا أنهينا الجدول بطريقة EndTable ،
// مؤشر منشئ المستندات موجود حاليًا خارج الجدول.
// هذا المؤشر له نفس وظيفة مؤشر النص الوامض في Microsoft Word.
// يمكن أيضًا نقله إلى موقع مختلف في المستند باستخدام أساليب MoveTo الخاصة بالباني.
// يمكننا تحريك المؤشر مرة أخرى داخل الجدول إلى خلية معينة.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


