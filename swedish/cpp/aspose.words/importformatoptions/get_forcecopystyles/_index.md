---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles metod"
linktitle: "get_ForceCopyStyles"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles metod. Hämtar eller anger ett booleskt värde som indikerar om konflikterande stilar ska kopieras i KeepSourceFormatting‑läge. Standardvärdet är false i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Hämtar eller anger ett booleskt värde som indikerar om konflikterande stilar ska kopieras i [KeepSourceFormatting](../../importformatmode/) läge. Standardvärdet är **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Anmärkningar


Som standard, om en motsvarande stil redan finns i ett destinationsdokument, expanderas källstilsformateringen till direkta nodattribut och stilens nod återställs till standard.

När detta alternativ är satt till **true** kommer källstilen att tvingas kopieras till destinationsdokumentet med ett unikt namn och tillämpas på den importerade noden.

Observera att i detta fall är det inte garanterat att formateringen av den importerade noden i destinationsdokumentet bevaras.

## Exempel



Visar hur man tvingat kopierar källstilar med unika namn.
```cpp
// Båda dokumenten innehåller MyStyle1 och MyStyle2, MyStyle3 finns endast i ett källdokument.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
