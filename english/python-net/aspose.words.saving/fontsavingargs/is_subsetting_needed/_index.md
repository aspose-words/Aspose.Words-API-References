---
title: is_subsetting_needed property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify whether the current font will be subsetted before exporting as a font resource."
type: docs
weight: 70
url: /python-net/aspose.words.saving/fontsavingargs/is_subsetting_needed/
---

## FontSavingArgs.is_subsetting_needed property

Allows to specify whether the current font will be subsetted before exporting as a font resource.

Fonts can be exported as complete original font files or subsetted to include only the characters
that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size 
with the one specified in [HtmlSaveOptions.font_resources_subsetting_size_threshold](../../htmlsaveoptions/font_resources_subsetting_size_threshold/). 
You can override this behavior for individual fonts by setting the [FontSavingArgs.is_subsetting_needed](./) property.




### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)

