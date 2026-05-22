---
title: ImportFormatOptions.resolve_theme_colors property
linktitle: resolve_theme_colors property
articleTitle: resolve_theme_colors property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.resolve_theme_colors property. Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly"
type: docs
weight: 90
url: /python-net/aspose.words/importformatoptions/resolve_theme_colors/
---

## ImportFormatOptions.resolve_theme_colors property

Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly.
The default value is ``False``.



```python
@property
def resolve_theme_colors(self) -> bool:
    ...

@resolve_theme_colors.setter
def resolve_theme_colors(self, value: bool):
    ...

```

### Remarks

Please note that this option is only relevant for the [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode.


Normally, Aspose.Words doesn't resolve source theme colors when importing styles can be preserved
without expanding formatting attributes into direct ones. However, in this case the actual colors
of the imported shapes can differ from the ones they had in the original document. The reason for
this is the different theme colors in the source and destination documents. Setting this option
to ``True`` forces to resolve source shape theme colors and hence to preserve the actual
color of the shapes they have in the source document.





### Examples

Shows how to import a node with resolving source theme colors of shapes.

```python
src_doc = aw.Document()
builder = aw.DocumentBuilder(doc=src_doc)
# Move to the primary footer and insert a shape that uses theme colors.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=50)
shape.stroke.fore_theme_color = aw.themes.ThemeColor.DARK1
dst_doc = aw.Document()
# Import the source footer into the destination document with theme colors resolved,
# so the shape preserves its actual color from the source document.
footer = src_doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.ImportFormatOptions()
options.resolve_theme_colors = True
imported_footer = dst_doc.import_node(src_node=footer, is_import_children=True, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options).as_header_footer()
dst_doc.first_section.headers_footers.add(imported_footer)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.ImportNodeWithResolveThemeColors.docx')
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

