---
title: FieldBuilder
second_title: Aspose.Words for C++ API Reference
description: Initializes an instance of the FieldBuilder class.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder.FieldBuilder method


Initializes an instance of the [FieldBuilder](../) class.

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | The type of the field to build. |

## Examples




Shows how to create and insert a field using a field builder. 
```cpp
auto doc = MakeObject<Document>();

// A convenient way of adding text content to a document is with a document builder.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Fields have their builder, which we can use to construct a field code piece by piece.
// In this case, we will construct a BARCODE field representing a US postal code,
// and then insert it in front of a Run.
auto fieldBuilder = MakeObject<FieldBuilder>(FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.CreateWithFieldBuilder.docx");
```

