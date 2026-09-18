---
title: "Aspose::Words::ParagraphFormat Klasse"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat Klasse. Stellt alle Formatierungen für einen Absatz dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 49000
url: /de/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Stellt die gesamte Formatierung eines Absatzes dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Setzt die Absatzformatierung auf die Standardwerte zurück. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Liest oder legt ein Flag fest, das angibt, ob der Zeichenabstand zwischen Bereichen lateinischen Textes und Bereichen ostasiatischen Textes im aktuellen Absatz automatisch angepasst wird. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Liest oder legt ein Flag fest, das angibt, ob der Zeichenabstand zwischen Zahlenbereichen und Bereichen ostasiatischen Textes im aktuellen Absatz automatisch angepasst wird. |
| [get_Alignment](./get_alignment/)() | Liest oder legt die Textausrichtung für den Absatz fest. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Liest oder legt die vertikale Position der Schriftart in einer Zeile fest. |
| [get_Bidi](./get_bidi/)() | Liest oder legt fest, ob dies ein rechts‑nach‑links‑Absatz ist. |
| [get_Borders](./get_borders/)() | Liest die Sammlung der Rahmen des Absatzes. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Liest oder legt den Wert (in Zeichen) für den Erstzeileneinzug oder hängenden Einzug fest. Verwenden Sie positive Werte, um den Erstzeileneinzug festzulegen, und negative Werte, um den hängenden Einzug festzulegen. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Liest oder legt den linken Einzugswert (in Zeichen) für die angegebenen Absätze fest. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Liest oder legt den rechten Einzugswert (in Zeichen) für die angegebenen Absätze fest. |
| [get_DropCapPosition](./get_dropcapposition/)() | Liest oder legt die Position für einen Initialbuchstaben‑Text fest. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Liest oder legt ein Flag fest, das angibt, ob ostasiatische Zeilenumbruchregeln auf den aktuellen Absatz angewendet werden. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Liest oder legt den Wert (in Punkten) für einen Erstzeileneinzug oder hängenden Einzug fest. Verwenden Sie positive Werte, um den Erstzeileneinzug festzulegen, und negative Werte, um den hängenden Einzug festzulegen. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Liest oder legt ein Flag fest, das angibt, ob hängende Interpunktion für den aktuellen Absatz aktiviert ist. |
| [get_IsHeading](./get_isheading/)() | Wahr, wenn der Absatzstil einer der integrierten Überschriftsstile ist. |
| [get_IsListItem](./get_islistitem/)() | Wahr, wenn der Absatz ein Element in einer Aufzählungs‑ oder Nummerierungsliste ist. |
| [get_KeepTogether](./get_keeptogether/)() | Wahr, wenn alle Zeilen im Absatz auf derselben Seite bleiben sollen. |
| [get_KeepWithNext](./get_keepwithnext/)() | Wahr, wenn der Absatz auf derselben Seite wie der nachfolgende Absatz bleiben soll. |
| [get_LeftIndent](./get_leftindent/)() | Liest oder legt den Wert (in Punkten) fest, der den linken Einzug für den Absatz darstellt. |
| [get_LineSpacing](./get_linespacing/)() | Liest oder legt den Zeilenabstand (in Punkten) für den Absatz fest. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Liest oder legt den Zeilenabstand für den Absatz fest. |
| [get_LinesToDrop](./get_linestodrop/)() | Liest oder legt die Anzahl der Zeilen des Absatztextes fest, die zur Berechnung der Initialbuchstaben‑Höhe verwendet werden. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Liest oder legt den Abstand (in Rasterlinien) nach den Absätzen fest. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Liest oder legt den Abstand (in Rasterlinien) vor den Absätzen fest. |
| [get_MirrorIndents](./get_mirrorindents/)() | Liest oder legt ein Flag fest, das angibt, ob der linke und rechte Einzug die gleiche Breite haben. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | Wenn **true**, werden [SpaceBefore](./get_spacebefore/) und [SpaceAfter](./get_spaceafter/) zwischen Absätzen desselben Stils ignoriert. |
| [get_OutlineLevel](./get_outlinelevel/)() | Gibt die Gliederungsebene des Absatzes im Dokument an. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | True, wenn ein Seitenumbruch vor dem Absatz erzwungen wird. |
| [get_RightIndent](./get_rightindent/)() | Liest oder setzt den Wert (in Punkten), der den rechten Einzug für den Absatz darstellt. |
| [get_Shading](./get_shading/)() | Gibt ein [Shading](../shading/)-Objekt zurück, das sich auf die Schattierungsformatierung des Absatzes bezieht. |
| [get_SnapToGrid](./get_snaptogrid/)() | Gibt an, ob der aktuelle Absatz die Dokumentgitterlinien‑pro‑Seite‑Einstellungen beim Layouten des Inhalts im Absatz verwenden soll. |
| [get_SpaceAfter](./get_spaceafter/)() | Liest oder setzt den Abstand (in Punkten) nach dem Absatz. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | True, wenn der Abstand nach dem Absatz automatisch festgelegt wird. |
| [get_SpaceBefore](./get_spacebefore/)() | Liest oder setzt den Abstand (in Punkten) vor dem Absatz. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | True, wenn der Abstand vor dem Absatz automatisch festgelegt wird. |
| [get_Style](./get_style/)() | Liest oder setzt den Absatzstil, der auf diese Formatierung angewendet wird. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Liest oder setzt den sprachunabhängigen Stilbezeichner des Absatzstils, der auf diese Formatierung angewendet wird. |
| [get_StyleName](./get_stylename/)() | Liest oder setzt den Namen des Absatzstils, der auf diese Formatierung angewendet wird. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Gibt an, ob der aktuelle Absatz von jeglicher Silbentrennung, die in den Dokumenteinstellungen angewendet wird, ausgenommen sein soll. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Gibt an, ob die Zeilen des aktuellen Absatzes von der Zeilennummerierung, die im übergeordneten Abschnitt angewendet wird, ausgenommen werden sollen. |
| [get_TabStops](./get_tabstops/)() | Liest die Sammlung benutzerdefinierter Tabulatoren, die für dieses Objekt definiert sind. |
| [get_WidowControl](./get_widowcontrol/)() | True, wenn die erste und letzte Zeile im Absatz auf derselben Seite wie der Rest des Absatzes bleiben sollen. |
| [get_WordWrap](./get_wordwrap/)() | Wenn diese Eigenschaft **false** ist, kann lateinischer Text in der Mitte eines Wortes im aktuellen Absatz umgebrochen werden. Andernfalls wird lateinischer Text wortweise umbrochen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Setter für [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Setter für [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Setter für [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Setter für [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Setter für [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Setter für [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Setter für [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter für [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Setter für [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter für [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Setter für [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und erhalten ein Dokumentenknoten ohne Kinder.
doc->RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
// Erstellen Sie zunächst einen neuen Abschnitt und fügen Sie ihn dann als Kind zum Wurzel-Dokumentenknoten hinzu.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt.
// auf der Seite zwischen der Kopf‑ und Fußzeile des Abschnitts.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Fügen Sie schließlich etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
// setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
