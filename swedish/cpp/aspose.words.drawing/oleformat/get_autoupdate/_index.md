---
title: "Aspose::Words::Drawing::OleFormat::get_AutoUpdate metod"
linktitle: "get_AutoUpdate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::get_AutoUpdate metod. Anger om länken till OLE-objektet automatiskt uppdateras eller inte i Microsoft Word i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing/oleformat/get_autoupdate/
---
## OleFormat::get_AutoUpdate method


Anger om länken till OLE-objektet automatiskt uppdateras eller inte i Microsoft Word.

```cpp
bool Aspose::Words::Drawing::OleFormat::get_AutoUpdate()
```

## Anmärkningar


Standardvärdet är **false**.

## Exempel



Visar hur man extraherar inbäddade OLE-objekt till filer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Vårt objekt uppdateras varken automatiskt eller är låst för uppdateringar.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// kan vi använda egenskapen "SuggestedExtension" för att bestämma vilken filändelse som ska tillämpas på filen.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Nedan följer två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 -  Spara det via en ström:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Spara det direkt till ett filnamn:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
