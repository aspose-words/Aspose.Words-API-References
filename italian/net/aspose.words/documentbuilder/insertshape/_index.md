---
title: DocumentBuilder.InsertShape
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce una forma in linea con tipo e dimensione specificati.
type: docs
weight: 440
url: /it/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(ShapeType, double, double) {#insertshape_1}

Inserisce una forma in linea con tipo e dimensione specificati.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeType | ShapeType | Il tipo di forma da inserire nel documento. |
| width | Double | La larghezza della forma in punti. |
| height | Double | L'altezza della forma in punti. |

### Valore di ritorno

Il nodo della forma che è stato inserito.

### Esempi

Mostra come inserire forme DML in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 - Galleggiante:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - In linea:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Se è necessario creare forme "non primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded o DiagonalCornersRounded,
// quindi salva il documento con conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertShape(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertshape}

Inserisce una forma mobile con posizione, dimensione e tipo di testo a capo specificati.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeType | ShapeType | Il tipo di forma da inserire nel documento |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza orizzontale dalla forma. |
| left | Double | Distanza in punti dall'origine al lato sinistro della forma. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza verticale dalla forma. |
| top | Double | Distanza in punti dall'origine al lato superiore della forma. |
| width | Double | La larghezza della forma in punti. |
| height | Double | La larghezza della forma in punti. |
| wrapType | WrapType | Specifica come disporre il testo attorno alla forma. |

### Valore di ritorno

Il nodo della forma che è stato inserito.

### Esempi

Mostra come inserire forme DML in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 - Galleggiante:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - In linea:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Se è necessario creare forme "non primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded o DiagonalCornersRounded,
// quindi salva il documento con conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


