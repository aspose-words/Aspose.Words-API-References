---
title: "Aspose::Words::DocumentBuilder::InsertFootnote method"
linktitle: "InsertFootnote"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertFootnote method. Infogar en fotnot eller slutnot i dokumentet i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Infogar en fotnot eller slutnot i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Anger om en fotnot eller en slutnot ska infogas. |
| footnoteText | const System::String\& | Anger texten för fotnoten. |

### ReturnValue

Returnerar ett fotnotobjekt som just skapats.

## Exempel



Visar hur man refererar text med en fotnot och en slutnot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga lite text och markera den med en fotnot där egenskapen IsAuto är inställd på "true" som standard,
// så att markören som ses i brödtexten automatiskt numreras till "1",
// och fotnoten kommer att visas längst ner på sidan.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Infoga mer text och markera den med en slutnot med en anpassad referensmarkör,
// som kommer att användas i stället för siffran "2" och sätta "IsAuto" till false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Fotnoter visas alltid längst ner på den text de refererar till,
// så att detta sidbrytning inte påverkar fotnoten.
// Å andra sidan är slutnoter alltid i slutet av dokumentet
// så att detta sidbrytning skjuter slutnoten ner till nästa sida.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## Se även

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Infogar en fotnot eller slutnot i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Anger om en fotnot eller en slutnot ska infogas. |
| footnoteText | const System::String\& | Anger texten för fotnoten. |
| referenceMark | const System::String\& | Anger den anpassade referensmarkeringen för fotnoten. |

### ReturnValue

Returnerar ett fotnotobjekt som just skapats.

## Exempel



Visar hur man refererar text med en fotnot och en slutnot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga lite text och markera den med en fotnot där egenskapen IsAuto är inställd på "true" som standard,
// så att markören som ses i brödtexten automatiskt numreras till "1",
// och fotnoten kommer att visas längst ner på sidan.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Infoga mer text och markera den med en slutnot med en anpassad referensmarkör,
// som kommer att användas i stället för siffran "2" och sätta "IsAuto" till false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Fotnoter visas alltid längst ner på den text de refererar till,
// så att detta sidbrytning inte påverkar fotnoten.
// Å andra sidan är slutnoter alltid i slutet av dokumentet
// så att detta sidbrytning skjuter slutnoten ner till nästa sida.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## Se även

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
