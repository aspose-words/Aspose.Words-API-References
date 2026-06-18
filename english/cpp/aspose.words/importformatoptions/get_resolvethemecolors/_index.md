---
title: Aspose::Words::ImportFormatOptions::get_ResolveThemeColors method
linktitle: get_ResolveThemeColors
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_ResolveThemeColors method. Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly. The default value is false in C++.'
type: docs
weight: 8500
url: /cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly. The default value is **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Remarks


Please note that this option is only relevant for the [KeepSourceFormatting](../../importformatmode/) mode.

Normally, Aspose.Words doesn't resolve source theme colors when importing styles can be preserved without expanding formatting attributes into direct ones. However, in this case the actual colors of the imported shapes can differ from the ones they had in the original document. The reason for this is the different theme colors in the source and destination documents. Setting this option to **true** forces to resolve source shape theme colors and hence to preserve the actual color of the shapes they have in the source document.

## Examples



Shows how to import a node with resolving source theme colors of shapes. 
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Move to the primary footer and insert a shape that uses theme colors.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Import the source footer into the destination document with theme colors resolved,
// so the shape preserves its actual color from the source document.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
