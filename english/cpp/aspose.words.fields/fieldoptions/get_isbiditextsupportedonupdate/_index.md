---
title: get_IsBidiTextSupportedOnUpdate
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the value indicating whether bidirectional text is fully supported during field update or not.
type: docs
weight: 157
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Ensure that any field operation involving right-to-left text is performs as expected.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Use a document builder to insert a field that contains the right-to-left text.
SharedPtr<FormField> comboBox = builder->InsertComboBox(u"MyComboBox", MakeArray<String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(ArtifactsDir + u"FieldOptions.Bidi.docx");
```

## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
