---
title: ConditionalStyleCollection.ClearFormatting
second_title: Aspose.Words لمراجع .NET API
description: ConditionalStyleCollection طريقة. مسح كافة الأنماط الشرطية لنمط الجدول.
type: docs
weight: 150
url: /ar/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

مسح كافة الأنماط الشرطية لنمط الجدول.

```csharp
public void ClearFormatting()
```

### أمثلة

يوضح كيفية إعادة تعيين أنماط الجدول الشرطي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// قم بتعيين نمط الجدول لتلوين حدود الصف الأول من الجدول باللون الأحمر.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// قم بتعيين نمط الجدول لتلوين حدود الصف الأخير من الجدول باللون الأزرق.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// فيما يلي طريقتان لاستخدام طريقة "ClearFormatting" لمسح الأنماط الشرطية.
// 1 - مسح الأنماط الشرطية لجزء معين من الجدول:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - امسح الأنماط الشرطية للجدول بأكمله:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### أنظر أيضا

* class [ConditionalStyleCollection](../)
* مساحة الاسم [Aspose.Words](../../conditionalstylecollection/)
* المجسم [Aspose.Words](../../../)


