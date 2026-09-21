---
title: "Aspose::Words::DocumentBase::ImportNode method"
linktitle: "ImportNode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase::ImportNode‑metod. Importerar en nod från ett annat dokument till det aktuella dokumentet i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Importerar en nod från ett annat dokument till det aktuella dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden som importeras. |
| isImportChildren | bool | **true** för att importera alla barnnoder rekursivt; annars **false**. |

### ReturnValue

Den klonade noden som tillhör det aktuella dokumentet.
## Anmärkningar


Denna metod använder alternativet [UseDestinationStyles](../../importformatmode/) för att lösa formatering.

Att importera en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras inte eller tas bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokument‑specifika egenskaper såsom referenser till stilar och listor från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av [InsertBefore1()</see> eller <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djupklon av källnoden.

## Exempel



Visar hur man importerar en nod från ett dokument till ett annat.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Varje nod har ett föräldradokument, vilket är det dokument som innehåller noden.
// Att infoga en nod i ett dokument som noden inte tillhör kommer att kasta ett undantag.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// Använd ImportNode‑metoden för att skapa en kopia av en nod, som kommer att ha dokumentet
// som anropade ImportNode‑metoden som sitt nya ägardokument.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Vi kan nu infoga noden i dokumentet.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## Se även

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formatering.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden att importeras. |
| isImportChildren | bool | **true** för att importera alla barnnoder rekursivt; annars **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |

### ReturnValue

Den klonade, importerade noden. Noden tillhör destinationsdokumentet, men har ingen förälder.
## Anmärkningar


Denna överlagring är användbar för att kontrollera hur stilar och listformatering importeras.

Att importera en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras inte eller tas bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokument‑specifika egenskaper såsom referenser till stilar och listor från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av [InsertBefore1()</see> eller <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djupklon av källnoden.

## Exempel



Visar hur man importerar en nod från källdokumentet till måldokumentet med specifika alternativ.
```cpp
// Skapa två dokument och lägg till en teckenstil i varje dokument.
// Konfigurera stilarna så att de har samma namn, men olika textformatering.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Importera avsnittet från måldokumentet till källdokumentet, vilket orsakar en stilnamnskonflikt.
// Om vi använder målstilar, så kommer den importerade källtexten med samma stilnamn
// som destinationstexten kommer att anta målstilen.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// Om vi använder ImportFormatMode.KeepDifferentStyles, bevaras källstilen,
// och namnkonflikten löses genom att lägga till ett suffix.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## Se även

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formatering.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden att importeras. |
| isImportChildren | bool | **true** för att importera alla barnnoder rekursivt; annars **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Tillåter att specificera olika ytterligare formateringsalternativ. |

### ReturnValue

Den klonade, importerade noden. Noden tillhör destinationsdokumentet, men har ingen förälder.
## Anmärkningar


Denna överlagring är användbar för att kontrollera hur stilar och listformatering importeras.

Att importera en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras inte eller tas bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokument‑specifika egenskaper såsom referenser till stilar och listor från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av [InsertBefore1()</see> eller <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djupklon av källnoden.

## Exempel



Visar hur man importerar en nod med upplösning av källans temafärger för former.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Gå till den primära sidfoten och infoga en form som använder temafärger.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importera källsidfoten till måldokumentet med temafärger upplösta,
// så att formen behåller sin faktiska färg från källdokumentet.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Se även

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
