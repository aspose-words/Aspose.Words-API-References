---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words para .NET
description: Limpie fácilmente los encabezados y pies de sección con el método ClearHeadersFooters. Optimice el diseño de su documento para una apariencia impecable.
type: docs
weight: 120
url: /es/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Borra los encabezados y pies de página de esta sección.

```csharp
public void ClearHeadersFooters()
```

## Observaciones

Se borra el texto de todos los encabezados y pies de página, pero[`HeaderFooter`](../../headerfooter/) Los objetos en sí no se eliminan.

Esto hace que los encabezados y pies de página de esta sección estén vinculados a los encabezados y pies de página de la sección anterior.

## Ejemplos

Muestra cómo borrar el contenido de todos los encabezados y pies de página de una sección.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Vacía todos los encabezados y pies de página de esta sección de todo su contenido.
// Los encabezados y pies de página seguirán presentes, pero no tendrán nada que mostrar.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Ver también

* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Borra los encabezados y pies de página de esta sección.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| preserveWatermarks | Boolean | Verdadero si no se eliminarán las marcas de agua. |

## Observaciones

Se borra el texto de todos los encabezados y pies de página, pero[`HeaderFooter`](../../headerfooter/) Los objetos en sí no se eliminan.

Esto hace que los encabezados y pies de página de esta sección estén vinculados a los encabezados y pies de página de la sección anterior.

## Ejemplos

Muestra cómo borrar el contenido del encabezado y pie de página con o sin marca de agua.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

//Agrega una marca de agua de texto simple.
doc.Watermark.SetText("Aspose Watermark");

// Asegúrese de que los encabezados y pies de página tengan contenido.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Elimina todo el contenido del encabezado y pie de página excepto las marcas de agua.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Elimina todo el contenido del encabezado y pie de página, incluidas las marcas de agua.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Ver también

* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
