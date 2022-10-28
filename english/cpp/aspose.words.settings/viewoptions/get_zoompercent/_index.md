---
title: get_ZoomPercent
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the percentage (between 10 and 500) at which you want to view your document.
type: docs
weight: 53
url: /cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions.get_ZoomPercent method


Gets or sets the percentage (between 10 and 500) at which you want to view your document.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```


If value is 0 then this property uses 100 instead, else if value is less than 10 or greater than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

## Examples




Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(ArtifactsDir + u"ViewOptions.SetZoomPercentage.doc");
```

