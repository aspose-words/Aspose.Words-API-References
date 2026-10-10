---
title: "Aspose::Words::StyleCollection::idx_get‑metod"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection::idx_get‑metod. Hämtar en inbyggd stil med dess språkoberoende identifierare i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Hämtar en inbyggd stil via dess språkoberoende identifierare.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Ett [StyleIdentifier](../../styleidentifier/)-värde som specificerar den inbyggda stil som ska hämtas. |
## Anmärkningar


När du får åtkomst till en stil som ännu inte finns skapas den automatiskt.

## Exempel



Visar hur man lägger till en [Style](../../style/) i ett dokuments stilsamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i denna samling.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena av
// dess egenskap "DefaultParagraphFormat" på stilens egenskap "ParagraphFormat".
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Lägg till en stil och verifiera sedan att den har standardinställningarna.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Se även

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Hämtar en stil efter namn eller alias.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Anmärkningar


Skiftlägeskänslig, returnerar **null** om stilen med det angivna namnet inte hittas.

Om detta är ett engelskt namn på en inbyggd stil som ännu inte finns skapas den automatiskt.

## Exempel



Visar när man ska beräkna om sidlayouten för dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Att spara ett dokument till PDF, till en bild eller skriva ut för första gången kommer automatiskt
// cacha layouten för dokumentet inom dess sidor.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Ändra dokumentet på något sätt.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// I den nuvarande versionen av Aspose.Words återuppbyggs inte dokumentet automatiskt när det ändras
// den cachade sidlayouten. Om vi vill att den cachade layouten
// ska hållas uppdaterad, måste vi uppdatera den manuellt.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Se även

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Hämtar en stil efter index.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Exempel



Visar hur man lägger till en [Style](../../style/) i ett dokuments stilsamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i denna samling.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena av
// dess egenskap "DefaultParagraphFormat" på stilens egenskap "ParagraphFormat".
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Lägg till en stil och verifiera sedan att den har standardinställningarna.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Se även

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
