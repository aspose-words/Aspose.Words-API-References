---
title: FileFormatUtil.contentTypeToLoadFormat method
linktitle: contentTypeToLoadFormat method
articleTitle: contentTypeToLoadFormat method
second_title: Aspose.Words for NodeJs
description: "FileFormatUtil.contentTypeToLoadFormat method. Converts IANA content type into a load format enumerated value."
type: docs
weight: 10
url: /nodejs-net/aspose.words/fileformatutil/contentTypeToLoadFormat/
---

## contentTypeToLoadFormat(contentType) {#string}

Converts IANA content type into a load format enumerated value.


```js
contentTypeToLoadFormat(contentType: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| contentType | string |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to find the corresponding Aspose load/save format from each media type string.

```js
// The ContentTypeToSaveFormat/ContentTypeToLoadFormat methods only accept official IANA media type names, also known as MIME types. 
// All valid media types are listed here: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Trying to associate a SaveFormat with a partial media type string will not work.
expect(() => aw.FileFormatUtil.contentTypeToSaveFormat("jpeg")).toThrow("Cannot convert this content type to a save format.");

// If Aspose.words does not have a corresponding save/load format for a content type, an exception will also be thrown.
expect(() => aw.FileFormatUtil.contentTypeToSaveFormat("application/zip")).toThrow("Cannot convert this content type to a save format.");

// Files of the types listed below can be saved, but not loaded using Aspose.words.
expect(() => aw.FileFormatUtil.contentTypeToLoadFormat("image/jpeg")).toThrow("Cannot convert this content type to a load format.");

expect(aw.FileFormatUtil.contentTypeToSaveFormat("image/jpeg")).toEqual(aw.SaveFormat.Jpeg);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("image/png")).toEqual(aw.SaveFormat.Png);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("image/tiff")).toEqual(aw.SaveFormat.Tiff);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("image/gif")).toEqual(aw.SaveFormat.Gif);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("image/x-emf")).toEqual(aw.SaveFormat.Emf);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("application/vnd.ms-xpsdocument")).toEqual(aw.SaveFormat.Xps);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("application/pdf")).toEqual(aw.SaveFormat.Pdf);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("image/svg+xml")).toEqual(aw.SaveFormat.Svg);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("application/epub+zip")).toEqual(aw.SaveFormat.Epub);

// For file types that can be saved and loaded, we can match a media type to both a load format and a save format.
expect(aw.FileFormatUtil.contentTypeToLoadFormat("application/msword")).toEqual(aw.LoadFormat.Doc);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("application/msword")).toEqual(aw.SaveFormat.Doc);

expect(aw.FileFormatUtil.contentTypeToLoadFormat( "application/vnd.openxmlformats-officedocument.wordprocessingml.document")).toEqual(aw.LoadFormat.Docx);
expect(aw.FileFormatUtil.contentTypeToSaveFormat( "application/vnd.openxmlformats-officedocument.wordprocessingml.document")).toEqual(aw.SaveFormat.Docx);

expect(aw.FileFormatUtil.contentTypeToLoadFormat("text/plain")).toEqual(aw.LoadFormat.Text);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("text/plain")).toEqual(aw.SaveFormat.Text);

expect(aw.FileFormatUtil.contentTypeToLoadFormat("application/rtf")).toEqual(aw.LoadFormat.Rtf);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("application/rtf")).toEqual(aw.SaveFormat.Rtf);

expect(aw.FileFormatUtil.contentTypeToLoadFormat("text/html")).toEqual(aw.LoadFormat.Html);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("text/html")).toEqual(aw.SaveFormat.Html);

expect(aw.FileFormatUtil.contentTypeToLoadFormat("multipart/related")).toEqual(aw.LoadFormat.Mhtml);
expect(aw.FileFormatUtil.contentTypeToSaveFormat("multipart/related")).toEqual(aw.SaveFormat.Mhtml);
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatUtil](../)

