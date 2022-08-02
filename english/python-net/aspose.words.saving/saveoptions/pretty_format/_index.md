---
title: pretty_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "When ``true``, pretty formats output where applicable"
type: docs
weight: 100
url: /python-net/aspose.words.saving/saveoptions/pretty_format/
---

## SaveOptions.pretty_format property

When ``true``, pretty formats output where applicable. 
Default value is **false**.


Set to **true** to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. 
Useful for testing or debugging.




### Examples

Shows how to enhance the readability of the raw code of a saved .html document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

html_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
html_options.pretty_format = use_pretty_format

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.pretty_format.html", html_options)

# Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
with open(ARTIFACTS_DIR + "HtmlSaveOptions.pretty_format.html", "rt", encoding="utf-8") as file:
    html = file.read()

if use_pretty_format:
    self.assertEqual(
        "<html>\n" +
            "\t<head>\n" +
                "\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />\n" +
                "\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />\n" +
                f"\t\t<meta name=\"generator\" content=\"{aw.BuildVersionInfo.product} {aw.BuildVersionInfo.version}\" />\n" +
                "\t\t<title>\n" +
                "\t\t</title>\n" +
            "\t</head>\n" +
            "\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">\n" +
                "\t\t<div>\n" +
                    "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\n" +
                        "\t\t\t\t<span>Hello world!</span>\n" +
                    "\t\t\t</p>\n" +
                    "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\n" +
                        "\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>\n" +
                    "\t\t\t</p>\n" +
                "\t\t</div>\n" +
            "\t</body>\n</html>",
        html)
else:
    self.assertEqual(
        "<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />" +
        "<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" +
        f"<meta name=\"generator\" content=\"{aw.BuildVersionInfo.product} {aw.BuildVersionInfo.version}\" /><title></title></head>" +
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
        "<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" +
        "<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>",
        html)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

