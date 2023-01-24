﻿---
title: use_gdi_raster_operations_emulation property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation."
type: docs
weight: 70
url: /python-net/aspose.words.saving/metafilerenderingoptions/use_gdi_raster_operations_emulation/
---

## MetafileRenderingOptions.use_gdi_raster_operations_emulation property

Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation.

Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation
comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to ``True``, Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to ``False``, Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is ``False``.




### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)
