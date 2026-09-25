---
title: Aspose::Words::Drawing::FillType enum
linktitle: FillType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::FillType enum. Specifies fill type for a fillable object in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.drawing/filltype/
---
## FillType enum


Specifies fill type for a fillable object.

```cpp
enum class FillType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Solid | 1 | Solid fill. |
| Patterned | 2 | Patterned fill. |
| Gradient | 3 | Gradient fill. |
| Textured | 4 | Textured fill. |
| Background | 5 | [Fill](../fill/) is the same as the background. |
| Picture | 6 | Picture fill. |


## Examples



Shows how to convert any of the fills back to solid fill. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Two color gradient.docx"));

// Get Fill object for Font of the first Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Check Fill properties of the Font.
System::Console::WriteLine(u"The type of the fill is: {0}", fill->get_FillType());
System::Console::WriteLine(u"The foreground color of the fill is: {0}", fill->get_ForeColor());
System::Console::WriteLine(u"The fill is transparent at {0}%", fill->get_Transparency() * 100);

// Change type of the fill to Solid with uniform green color.
fill->Solid();
System::Console::WriteLine(u"\nThe fill is changed:");
System::Console::WriteLine(u"The type of the fill is: {0}", fill->get_FillType());
System::Console::WriteLine(u"The foreground color of the fill is: {0}", fill->get_ForeColor());
System::Console::WriteLine(u"The fill transparency is {0}%", fill->get_Transparency() * 100);

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
