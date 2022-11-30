---
title: get_IgnoreDmlUniqueId
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to ignore difference in DrawingML unique Id. Default value is false.
type: docs
weight: 53
url: /cpp/aspose.words.comparing/compareoptions/get_ignoredmluniqueid/
---
## CompareOptions::get_IgnoreDmlUniqueId method


Specifies whether to ignore difference in DrawingML unique Id. Default value is **false**.

```cpp
bool Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId() const
```


## Examples



Shows how to compare documents ignoring DML unique ID. 
```cpp
auto docA = MakeObject<Document>(MyDir + u"DML unique ID original.docx");
auto docB = MakeObject<Document>(MyDir + u"DML unique ID compare.docx");

// By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
// If we are ignoring DML's unique ID, and revisions count were 0.
auto compareOptions = MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## See Also

* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words](../../../)
