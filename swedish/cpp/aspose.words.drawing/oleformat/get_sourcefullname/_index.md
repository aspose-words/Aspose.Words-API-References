---
title: "Aspose::Words::Drawing::OleFormat::get_SourceFullName method"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::get_SourceFullName method. Hämtar eller anger sökvägen och namnet på källfilen för det länkade OLE-objektet i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.drawing/oleformat/get_sourcefullname/
---
## OleFormat::get_SourceFullName method


Hämtar eller anger sökväg och namn för källfilen för det länkade OLE-objektet.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SourceFullName()
```

## Anmärkningar


Standardvärdet är en tom sträng.

Om [SourceFullName](./) inte är en tom sträng är OLE-objektet länkat.

## Exempel



Visar hur man infogar länkade och olänkade OLE-objekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bädda in en Microsoft Visio-ritning i dokumentet som ett OLE-objekt.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Infoga en länk till filen i det lokala filsystemet och visa den som en ikon.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// Infogning av OLE-objekt skapar former som lagrar dessa objekt.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Om en form innehåller ett OLE-objekt kommer den att ha en giltig \"OleFormat\"-egenskap,
// vilken vi kan använda för att verifiera vissa aspekter av formen.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Om objektet innehåller OLE-data kan vi komma åt det med en ström.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
