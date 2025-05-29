---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words لـ .NET
description: أضف أشكالًا مضمنة مخصصة بسهولة باستخدام طريقة InsertShape في DocumentBuilder. حسّن مستنداتك بمؤثرات بصرية مصممة خصيصًا لعروض تقديمية مؤثرة!
type: docs
weight: 460
url: /ar/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

إدراج شكل مضمن بنوع وحجم محددين.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| shapeType | ShapeType | نوع الشكل الذي سيتم إدراجه في المستند. |
| width | Double | عرض الشكل بالنقاط. |
| height | Double | ارتفاع الشكل بالنقاط. |

### قيمة الإرجاع

عقدة الشكل التي تم إدراجها.

## أمثلة

يوضح كيفية إدراج أشكال DML في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من التغليف الذي قد تمتلكه الأشكال.
// 1 - عائم:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - مضمن:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة إلى إنشاء أشكال "غير بدائية"، مثل SingleCornerSnipped وTopCornersSnipped وDiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند بالتوافق "الصارم" أو "الانتقالي"، والذي يسمح بحفظ الشكل كـ DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

إدراج شكل عائم حر مع موضع وحجم ونوع التفاف النص المحدد.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| shapeType | ShapeType | نوع الشكل الذي سيتم إدراجه في المستند |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم قياس المسافة الأفقية إلى الشكل منه. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر للشكل. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة الرأسية إلى الشكل منه. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي للشكل. |
| width | Double | عرض الشكل بالنقاط. |
| height | Double | ارتفاع الشكل بالنقاط. |
| wrapType | WrapType | يحدد كيفية لف النص حول الشكل. |

### قيمة الإرجاع

عقدة الشكل التي تم إدراجها.

## أمثلة

يوضح كيفية إدراج أشكال DML في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من التغليف الذي قد تمتلكه الأشكال.
// 1 - عائم:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - مضمن:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة إلى إنشاء أشكال "غير بدائية"، مثل SingleCornerSnipped وTopCornersSnipped وDiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند بالتوافق "الصارم" أو "الانتقالي"، والذي يسمح بحفظ الشكل كـ DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
