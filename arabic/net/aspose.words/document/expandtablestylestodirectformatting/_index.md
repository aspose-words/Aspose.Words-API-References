---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words لـ .NET
description: قم بتحويل أنماط الجدول إلى تنسيق مباشر باستخدام طريقة ExpandTableStylesToDirectFormatting، مما يعمل على تحسين مظهر مستندك بسهولة.
type: docs
weight: 630
url: /ar/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

يحول التنسيق المحدد في أنماط الجدول إلى تنسيق مباشر على الجداول في المستند.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## ملاحظات

هذه الطريقة موجودة لأن هذا الإصدار من Aspose.Words لا يوفر سوى دعم محدود لأنماط جداول x000d_ (انظر أدناه). قد تكون هذه الطريقة مفيدة عند تحميل مستند DOCX أو WordprocessingML يحتوي على جداول مُنسقة بأنماط جداول، وتحتاج إلى الاستعلام عن تنسيق جداول x000d_ أو الخلايا أو الفقرات أو النصوص.

يوفر هذا الإصدار من Aspose.Words دعمًا محدودًا لأنماط الجدول على النحو التالي:

* يتم الاحتفاظ بأنماط الجدول المحددة في مستندات DOCX أو WordprocessingML كـ table styles عند حفظ المستند بتنسيق DOCX أو WordprocessingML.
* يتم تحويل أنماط الجدول المحددة في مستندات DOCX أو WordprocessingML تلقائيًا إلى تنسيق مباشر على الجداول عند حفظ المستند بأي تنسيق آخر أو عرضه أو طباعته.
* يتم الاحتفاظ بأنماط الجدول المحددة في مستندات DOC كأنماط جدول عند حفظ المستند بتنسيق DOC فقط.

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

//تتعلق هذه الطريقة بخصائص نمط الجدول مثل تلك التي قمنا بتعيينها أعلاه.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
