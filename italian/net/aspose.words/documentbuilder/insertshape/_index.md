---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words per .NET
description: Aggiungi facilmente forme personalizzate in linea con il metodo InsertShape di DocumentBuilder. Arricchisci i tuoi documenti con elementi visivi personalizzati per presentazioni di grande impatto!
type: docs
weight: 460
url: /it/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Inserisce una forma in linea con il tipo e le dimensioni specificati.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeType | ShapeType | Tipo di forma da inserire nel documento. |
| width | Double | Larghezza della forma in punti. |
| height | Double | L'altezza della forma in punti. |

### Valore di ritorno

Il nodo forma che è stato inserito.

## Esempi

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
// AngoliTopUnoArrotondatoUnoTagliato, AngoloSingoloArrotondato, AngoliTopArrotondati o AngoliDiagonaliArrotondati,
// quindi salvare il documento con conformità "Rigorosa" o "Transizionale", che consente di salvare la forma come DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Inserisce una forma mobile con posizione, dimensione e tipo di avvolgimento del testo specificati.

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
| width | Double | Larghezza della forma in punti. |
| height | Double | L'altezza della forma in punti. |
| wrapType | WrapType | Specifica come disporre il testo attorno alla forma. |

### Valore di ritorno

Il nodo forma che è stato inserito.

## Esempi

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
// AngoliTopUnoArrotondatoUnoTagliato, AngoloSingoloArrotondato, AngoliTopArrotondati o AngoliDiagonaliArrotondati,
// quindi salvare il documento con conformità "Rigorosa" o "Transizionale", che consente di salvare la forma come DML.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
