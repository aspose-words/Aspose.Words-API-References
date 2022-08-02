---
title: force_copy_styles property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode"
type: docs
weight: 20
url: /python-net/aspose.words/importformatoptions/force_copy_styles/
---

## ImportFormatOptions.force_copy_styles property

Gets or sets a boolean value indicating either to copy conflicting styles
in [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode.
The default value is ``false``.


By default, if a matching style already exists in a destination document, the source style formatting
is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to ``true``, the source style will be forcibly copied
into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document
will be preserved.




### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

