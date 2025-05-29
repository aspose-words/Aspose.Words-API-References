---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: .NET için Aspose.Words
description: DocumentBuilder'ın InsertGroupShape yöntemi ile şekilleri zahmetsizce gruplandırın. Yeni GroupShape düğümlerini sorunsuz bir şekilde ekleyerek düzenli tasarımlar oluşturun.
type: docs
weight: 360
url: /tr/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Parametre olarak geçirilen şekilleri, geçerli konuma eklenen yeni bir GroupShape düğümüne gruplandırır.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| shapes | ShapeBase[] | Gruplandırılacak şekillerin listesi. |

## Notlar

Yeni GroupShape'in konumu ve boyutu otomatik olarak hesaplanacaktır.

VML ve DML şekilleri birlikte gruplandırılamaz.

## Örnekler

Grup şeklinin şekille nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Şekilleri belirtilen konuma eklenen bir GroupShape düğümünde birleştir.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Shape ve GroupShape düğümlerini birleştir.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

DML grup şeklinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Yeni GroupShape düğümünün boyutları.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Belirtilen konuma eklenen belirtilen boyuttaki GroupShape düğümünü ekle.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Pozisyonu ve boyutu otomatik olarak hesaplanacak olan GroupShape düğümünü ekle.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Ayrıca bakınız

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Belirtilen boyuttaki yeni bir GroupShape düğümüne parametre olarak geçirilen şekilleri gruplandırır ve belirtilen konuma eklenir.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| left | Double | Grup şeklinin başlangıç noktasından sol tarafa kadar olan mesafe. |
| top | Double | Grup şeklinin başlangıç noktasından üst kenarına kadar olan mesafe. |
| width | Double | Grup şeklinin puan cinsinden genişliği. Negatif bir değere izin verilmez. |
| height | Double | Grup şeklinin puan cinsinden yüksekliği. Negatif bir değere izin verilmez. |
| shapes | ShapeBase[] | Gruplandırılacak şekillerin listesi. |

## Notlar

VML ve DML şekilleri birlikte gruplandırılamaz.

## Örnekler

DML grup şeklinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Yeni GroupShape düğümünün boyutları.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Belirtilen konuma eklenen belirtilen boyuttaki GroupShape düğümünü ekle.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Pozisyonu ve boyutu otomatik olarak hesaplanacak olan GroupShape düğümünü ekle.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Ayrıca bakınız

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
