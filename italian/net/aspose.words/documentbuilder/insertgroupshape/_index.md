---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words per .NET
description: Raggruppa le forme senza sforzo con il metodo InsertGroupShape di DocumentBuilder. Crea progetti organizzati inserendo nuovi nodi GroupShape senza soluzione di continuità.
type: docs
weight: 360
url: /it/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Raggruppa le forme passate come parametro in un nuovo nodo GroupShape che viene inserito nella posizione corrente.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapes | ShapeBase[] | Elenco delle forme da raggruppare. |

## Osservazioni

La posizione e la dimensione del nuovo GroupShape verranno calcolate automaticamente.

Le forme VML e DML non possono essere raggruppate.

## Esempi

Mostra come combinare la forma del gruppo con la forma.

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

// Combina le forme in un nodo GroupShape che viene inserito nella posizione specificata.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Combina i nodi Shape e GroupShape.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

Mostra come inserire una forma di gruppo DML.

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

// Dimensioni per il nuovo nodo GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Inserisce il nodo GroupShape per la dimensione specificata, che viene inserito nella posizione specificata.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Inserisce il nodo GroupShape la cui posizione e dimensione verranno calcolate automaticamente.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Guarda anche

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Raggruppa le forme passate come parametro in un nuovo nodo GroupShape della dimensione specificata che viene inserito nella posizione specificata.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| left | Double | Distanza in punti dall'origine al lato sinistro della forma del gruppo. |
| top | Double | Distanza in punti dall'origine al lato superiore della forma del gruppo. |
| width | Double | Larghezza della forma del gruppo in punti. Non è consentito un valore negativo. |
| height | Double | Altezza della forma del gruppo in punti. Non è consentito un valore negativo. |
| shapes | ShapeBase[] | Elenco delle forme da raggruppare. |

## Osservazioni

Le forme VML e DML non possono essere raggruppate insieme.

## Esempi

Mostra come inserire una forma di gruppo DML.

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

// Dimensioni per il nuovo nodo GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Inserisce il nodo GroupShape per la dimensione specificata, che viene inserito nella posizione specificata.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Inserisce il nodo GroupShape la cui posizione e dimensione verranno calcolate automaticamente.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Guarda anche

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
