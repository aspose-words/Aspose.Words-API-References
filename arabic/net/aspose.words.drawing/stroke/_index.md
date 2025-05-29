---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Stroke لتحسين أشكالك باستخدام ضربات قابلة للتخصيص، مما يضيف لمسة احترافية إلى مستنداتك بسهولة.
type: docs
weight: 1720
url: /ar/net/aspose.words.drawing/stroke/
---
## Stroke class

يحدد خطًا للشكل.

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public class Stroke
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | يحصل على لون الخلفية للخط أو يعينه. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون خلفية الحد. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | يحصل على أو يعين قيمة مزدوجة لتفتيح أو تعتيم لون خلفية الخط. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | يحصل على لون المقدمة الأساسي للخط بدون أي تعديلات. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | يحدد لون الخط. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | يحدد لونًا ثانيًا للخط. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | يحدد نمط النقطة والشرطة للخط. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | يحدد طول رأس السهم لنهاية الخط. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | يحدد رأس السهم لنهاية الخط. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | يحدد عرض رأس السهم لنهاية الخط. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | يحدد نمط الغطاء لنهاية الخط. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | يحصل على تنسيق التعبئة لـ`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | يحصل على لون المقدمة للخط أو يعينه. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون المقدمة للحدود. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | يحصل على أو يعين قيمة مزدوجة لتفتيح أو تغميق لون مقدمة الخط. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | يحدد الصورة لصورة الحد أو تعبئة النمط. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | يحدد نمط الانضمام للخط المتعدد. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | يحدد نمط خط الرسم. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | يحدد ما إذا كان سيتم رسم المسار أم لا. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | يُحدد مقدار شفافية الخط. النطاق الصحيح من 0 إلى 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | يحدد طول رأس السهم لبداية الضربة. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | يحدد رأس السهم لبداية الضربة. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | يحدد عرض رأس السهم لبداية الضربة. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | يحصل على قيمة أو يعينها بين 0.0 (غير شفاف) و1.0 (واضح) تمثل درجة شفافية للخط. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كانت الخط مرئيًا أم لا. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | يحدد سمك الفرشاة التي ترسم مسار الشكل بالنقاط. |

## ملاحظات

استخدم[`Stroke`](../shape/stroke/)الخاصية للوصول إلى خصائص حدود الشكل. لا تقم بإنشاء مثيلات من`Stroke` الصف مباشرة.

## أمثلة

يوضح كيفية تغيير خصائص السكتة الدماغية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

//الأشكال الأساسية، مثل المستطيل، تحتوي على جزأين مرئيين.
// 1 - التعبئة، والتي تنطبق على المنطقة داخل مخطط الشكل:
shape.Fill.ForeColor = Color.White;

// 2 - الخط الذي يحدد الخطوط العريضة للشكل:
// تعديل خصائص مختلفة لخط هذا الشكل.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
