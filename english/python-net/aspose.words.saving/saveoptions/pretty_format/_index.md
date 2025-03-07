---
title: SaveOptions.pretty_format property
linktitle: pretty_format property
articleTitle: pretty_format property
second_title: Aspose.Words for Python
description: "SaveOptions.pretty_format property. When ``True``, pretty formats output where applicable"
type: docs
weight: 90
url: /python-net/aspose.words.saving/saveoptions/pretty_format/
---

## SaveOptions.pretty_format property

When ``True``, pretty formats output where applicable.
Default value is ``False``.



```python
@property
def pretty_format(self) -> bool:
    ...

@pretty_format.setter
def pretty_format(self, value: bool):
    ...

```

### Remarks

Set to ``True`` to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable.
Useful for testing or debugging.




### Examples

Shows how to enhance the readability of the raw code of a saved .html document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
html_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
html_options.pretty_format = use_pretty_format
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.PrettyFormat.html', save_options=html_options)
# Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
html = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.PrettyFormat.html')
new_line = system_helper.environment.Environment.new_line()
if use_pretty_format:
    self.assertEqual(f'<html>{new_line}' + f'\t<head>{new_line}' + f'\t\t<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />{new_line}' + f'\t\t<meta http-equiv="Content-Style-Type" content="text/css" />{new_line}' + f'\t\t<meta name="generator" content="{aw.BuildVersionInfo.product} {aw.BuildVersionInfo.version}" />{new_line}' + f'\t\t<title>{new_line}' + f'\t\t</title>{new_line}' + f'\t</head>{new_line}' + f"""\t<body style="font-family:'Times New Roman'; font-size:12pt">{new_line}""" + f'\t\t<div>{new_line}' + f'\t\t\t<p style="margin-top:0pt; margin-bottom:0pt">{new_line}' + f'\t\t\t\t<span>Hello world!</span>{new_line}' + f'\t\t\t</p>{new_line}' + f'\t\t\t<p style="margin-top:0pt; margin-bottom:0pt">{new_line}' + f'\t\t\t\t<span style="-aw-import:ignore">&#xa0;</span>{new_line}' + f'\t\t\t</p>{new_line}' + f'\t\t</div>{new_line}' + f'\t</body>{new_line}</html>', html)
else:
    self.assertEqual('<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8" />' + '<meta http-equiv="Content-Style-Type" content="text/css" />' + f'<meta name="generator" content="{aw.BuildVersionInfo.product} {aw.BuildVersionInfo.version}" /><title></title></head>' + '<body style="font-family:\'Times New Roman\'; font-size:12pt">' + '<div><p style="margin-top:0pt; margin-bottom:0pt"><span>Hello world!</span></p>' + '<p style="margin-top:0pt; margin-bottom:0pt"><span style="-aw-import:ignore">&#xa0;</span></p></div></body></html>', html)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

