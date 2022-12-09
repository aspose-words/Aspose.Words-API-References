---
title: get_FormsDesign
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the document is in forms design mode.
type: docs
weight: 40
url: /cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Specifies whether the document is in forms design mode.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Remarks


Currently works only for documents in WordML format.

## Examples



Shows how to enable/disable forms design mode. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Set the "FormsDesign" property to "false" to keep forms design mode disabled.
// Set the "FormsDesign" property to "true" to enable forms design mode.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(ArtifactsDir + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(ArtifactsDir + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## See Also

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words](../../../)
