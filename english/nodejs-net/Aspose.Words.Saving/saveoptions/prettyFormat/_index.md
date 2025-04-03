---
title: SaveOptions.prettyFormat property
linktitle: prettyFormat property
articleTitle: prettyFormat property
second_title: Aspose.Words for NodeJs
description: "SaveOptions.prettyFormat property. When ``true``, pretty formats output where applicable"
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Saving/saveoptions/prettyFormat/
---

## SaveOptions.prettyFormat property

When ``true``, pretty formats output where applicable.
Default value is ``false``.



```js
get prettyFormat(): boolean
```

### Remarks

Set to ``true`` to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable.
Useful for testing or debugging.




### Examples

Shows how to enhance the readability of the raw code of a saved .html document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

let htmlOptions = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
htmlOptions.prettyFormat = usePrettyFormat;

doc.save(base.artifactsDir + "HtmlSaveOptions.prettyFormat.html", htmlOptions);

// Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
let html = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.prettyFormat.html").toString();

if (usePrettyFormat)
  expect(html).toEqual(
    "<html>\r\n" +
          "\t<head>\r\n" +
            "\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />\r\n" +
            "\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />\r\n" +
            `\t\t<meta name=\"generator\" content=\"${aw.BuildVersionInfo.product} ${aw.BuildVersionInfo.version}\" />\r\n` +
            "\t\t<title>\r\n" +
            "\t\t</title>\r\n" +
          "\t</head>\r\n" +
          "\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">\r\n" +
            "\t\t<div>\r\n" +
              "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                "\t\t\t\t<span>Hello world!</span>\r\n" +
              "\t\t\t</p>\r\n" +
              "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                "\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>\r\n" +
              "\t\t\t</p>\r\n" +
            "\t\t</div>\r\n" +
          "\t</body>\r\n</html>");
else
  expect(html).toEqual(
    "<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />" +
        "<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" +
        `<meta name=\"generator\" content=\"${aw.BuildVersionInfo.product} ${aw.BuildVersionInfo.version}\" /><title></title></head>` +
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
        "<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" +
        "<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

