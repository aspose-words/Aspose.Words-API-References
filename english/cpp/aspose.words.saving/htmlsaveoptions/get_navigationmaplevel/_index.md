---
title: Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel method
linktitle: get_NavigationMapLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel method. Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is %3 in C++.'
type: docs
weight: 40500
url: /cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Remarks


The navigation map allows user agents to provide an easy way of navigation through the document structure. Usually navigation points correspond to headings in the document. In order to populate headings up to level **N** assign this value to [NavigationMapLevel](./).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2** and **Heading 3**. You can set this property to a value from 1 to 9 in order to request the corresponding maximum level. Setting it to zero will reduce the navigation map to only the document root or roots of document parts. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
