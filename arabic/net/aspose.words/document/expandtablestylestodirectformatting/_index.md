---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words لـ .NET
description: Document ExpandTableStylesToDirectFormatting طريقة. تحويل التنسيق المحدد في أنماط الجدول إلى تنسيق مباشر على الجداول في المستند في C#.
type: docs
weight: 590
url: /ar/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

تحويل التنسيق المحدد في أنماط الجدول إلى تنسيق مباشر على الجداول في المستند.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## ملاحظات

توجد هذه الطريقة لأن هذا الإصدار من Aspose.Words يوفر دعمًا محدودًا فقط لأنماط الجدول (انظر أدناه). قد تكون هذه الطريقة مفيدة عند تحميل مستند DOCX أو WordprocessingML الذي يحتوي على جداول منسقة باستخدام أنماط الجدول وتحتاج إلى الاستعلام عن تنسيق الجداول أو الخلايا أو الفقرات أو النص .

يوفر هذا الإصدار من Aspose.Words دعمًا محدودًا لأنماط الجدول كما يلي:

* يتم الاحتفاظ بأنماط الجدول المحددة في مستندات DOCX أو WordprocessingML كأنماط جدول عند حفظ المستند كـ DOCX أو WordprocessingML.
* يتم تحويل أنماط الجدول المحددة في مستندات DOCX أو WordprocessingML تلقائيًا إلى تنسيق مباشر على الجداول عند حفظ المستند في أي تنسيق آخر، أو للعرض أو الطباعة.
* يتم الاحتفاظ بأنماط الجدول المحددة في مستندات DOC كأنماط جدول عند حفظ المستند كـ DOC فقط.

## أمثلة

يوضح كيفية تطبيق خصائص نمط الجدول مباشرة على عناصر الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// تتعلق هذه الطريقة بخصائص نمط الجدول مثل تلك التي حددناها أعلاه.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
