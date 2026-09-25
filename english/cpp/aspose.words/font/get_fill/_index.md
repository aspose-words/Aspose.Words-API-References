---
title: Aspose::Words::Font::get_Fill method
linktitle: get_Fill
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Fill method. Gets fill formatting for the Font in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words/font/get_fill/
---
## Font::get_Fill method


Gets fill formatting for the [Font](../).

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Font::get_Fill()
```


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

* Class [Fill](../../../aspose.words.drawing/fill/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
