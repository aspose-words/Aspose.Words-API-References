---
title: InsertImage
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 350
url: /net/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder.InsertImage method (1 of 12)

Inserts an image from a .NET Image object into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(Image image)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image to insert into the document. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (2 of 12)

Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The file with the image. Can be any valid local or remote URI. |

## Return Value

The image node that was just inserted.

### Remarks

This overload will automatically download the image before inserting into the document if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (3 of 12)

Inserts an image from a stream into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (4 of 12)

Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The byte array that contains the image. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (5 of 12)

Inserts an inline image from a .NET Image object into the document and scales it to the specified size.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image to insert into the document. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (6 of 12)

Inserts an inline image from a file or URL into the document and scales it to the specified size.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The file that contains the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (7 of 12)

Inserts an inline image from a stream into the document and scales it to the specified size.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (8 of 12)

Inserts an inline image from a byte array into the document and scales it to the specified size.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The byte array that contains the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (9 of 12)

Inserts an image from a .NET Image object at the specified position and size.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image to insert into the document. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (10 of 12)

Inserts an image from a file or URL at the specified position and size.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The file that contains the image. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (11 of 12)

Inserts an image from a stream at the specified position and size.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertImage method (12 of 12)

Inserts an image from a byte array at the specified position and size.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The byte array that contains the image. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

## Return Value

The image node that was just inserted.

### Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
