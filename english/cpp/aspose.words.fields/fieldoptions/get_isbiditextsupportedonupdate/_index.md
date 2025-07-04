---
title: Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate method
linktitle: get_IsBidiTextSupportedOnUpdate
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate method. Gets or sets the value indicating whether bidirectional text is fully supported during field update or not in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Gets or sets the value indicating whether bidirectional text is fully supported during field update or not.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Remarks


When this property is set to **true**, additional steps are performed to produce Right-To-Left language (i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to **false** and Right-To-Left language is used, correctness of field result after its update is not guaranteed.

The default value is **false**.

## Examples



Shows how to use [FieldOptions](../) to ensure that field updating fully supports bi-directional text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ensure that any field operation involving right-to-left text is performs as expected.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Use a document builder to insert a field that contains the right-to-left text.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
