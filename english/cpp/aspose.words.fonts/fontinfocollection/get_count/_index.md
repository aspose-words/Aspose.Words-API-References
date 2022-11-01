---
title: get_Count
second_title: Aspose.Words for C++ API Reference
description: Gets the number of elements contained in the collection.
type: docs
weight: 66
url: /cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection.get_Count method


Gets the number of elements contained in the collection.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## Examples




Shows info about the fonts that are present in the blank document. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains 3 default fonts. Each font in the document
// will have a corresponding FontInfo object which contains details about that font.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

