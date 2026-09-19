---
title: "classe Aspose::Words::Font"
linktitle: "Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Font. Contiene gli attributi del carattere (nome del carattere, dimensione, colore, ecc.) per un oggetto. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words/font/
---
## Font class


Contiene attributi del carattere (nome del carattere, dimensione del carattere, colore e così via) per un oggetto. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Ripristina la formattazione predefinita del carattere. |
| [get_AllCaps](./get_allcaps/)() | Vero se il carattere è formattato tutto in maiuscolo. |
| [get_AutoColor](./get_autocolor/)() | Restituisce il colore calcolato attuale del testo (nero o bianco) da utilizzare per 'auto color'. Se il colore non è 'auto' restituisce [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | Specifica se il contenuto di questa sequenza deve avere caratteristiche da destra a sinistra. |
| [get_Bold](./get_bold/)() | Vero se il carattere è formattato in grassetto. |
| [get_BoldBi](./get_boldbi/)() | Vero se il testo da destra a sinistra è formattato in grassetto. |
| [get_Border](./get_border/)() | Restituisce un oggetto [Border](../border/) che specifica il bordo per il carattere. |
| [get_Color](./get_color/)() | Ottiene o imposta il colore del carattere. |
| [get_ComplexScript](./get_complexscript/)() | Specifica se il contenuto di questa sequenza deve essere trattato come testo a script complesso indipendentemente dai valori dei caratteri Unicode quando si determina la formattazione per questa sequenza. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | Vero se il carattere è formattato con doppia barratura. |
| [get_Emboss](./get_emboss/)() | Vero se il carattere è formattato in rilievo. |
| [get_EmphasisMark](./get_emphasismark/)() | Ottiene o imposta il segno di enfasi applicato a questa formattazione. |
| [get_Engrave](./get_engrave/)() | Vero se il carattere è formattato incavato. |
| [get_Fill](./get_fill/)() | Ottiene la formattazione di riempimento per il [Font](./). |
| [get_Hidden](./get_hidden/)() | Vero se il carattere è formattato come testo nascosto. |
| [get_HighlightColor](./get_highlightcolor/)() | Ottiene o imposta il colore di evidenziazione (marcatore). |
| [get_Italic](./get_italic/)() | Vero se il carattere è formattato in corsivo. |
| [get_ItalicBi](./get_italicbi/)() | Vero se il testo da destra a sinistra è formattato in corsivo. |
| [get_Kerning](./get_kerning/)() | Ottiene o imposta la dimensione del carattere a partire dalla quale inizia il kerning. |
| [get_LineSpacing](./get_linespacing/)() | Restituisce l'interlinea di questo carattere (in punti). |
| [get_LocaleId](./get_localeid/)() | Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati. |
| [get_LocaleIdBi](./get_localeidbi/)() | Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati da destra a sinistra. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Ottiene o imposta l'identificatore locale (lingua) dei caratteri asiatici formattati. |
| [get_Name](./get_name/)() | Ottiene o imposta il nome del carattere. |
| [get_NameAscii](./get_nameascii/)() | Restituisce o imposta il carattere usato per il testo latino (caratteri con codici da 0 (zero) a 127). |
| [get_NameBi](./get_namebi/)() | Restituisce o imposta il nome del carattere in un documento in lingua da destra a sinistra. |
| [get_NameFarEast](./get_namefareast/)() | Restituisce o imposta un nome di carattere dell'Est asiatico. |
| [get_NameOther](./get_nameother/)() | Restituisce o imposta il font usato per i caratteri con codici da 128 a 255. |
| [get_NoProofing](./get_noproofing/)() | True quando i caratteri formattati non devono essere controllati ortograficamente. |
| [get_NumberSpacing](./get_numberspacing/)() | Ottiene o imposta il tipo di spaziatura del numero visualizzato. |
| [get_Outline](./get_outline/)() | True se il font è formattato come contorno. |
| [get_Position](./get_position/)() | Ottiene o imposta la posizione del testo (in punti) rispetto alla linea di base. Un numero positivo solleva il testo, e un numero negativo lo abbassa. |
| [get_Scaling](./get_scaling/)() | Ottiene o imposta la scala della larghezza dei caratteri in percentuale. |
| [get_Shading](./get_shading/)() | Restituisce un oggetto [Shading](../shading/) che si riferisce alla formattazione dell'ombreggiatura per il font. |
| [get_Shadow](./get_shadow/)() | True se il font è formattato come ombreggiato. |
| [get_Size](./get_size/)() | Ottiene o imposta la dimensione del font in punti. |
| [get_SizeBi](./get_sizebi/)() | Ottiene o imposta la dimensione del font in punti usata in un documento da destra a sinistra. |
| [get_SmallCaps](./get_smallcaps/)() | True se il font è formattato come lettere maiuscole piccole. |
| [get_SnapToGrid](./get_snaptogrid/)() | Specifica se il font corrente deve utilizzare le impostazioni di caratteri per riga della griglia del documento durante il layout. |
| [get_Spacing](./get_spacing/)() | Restituisce o imposta la spaziatura (in punti) tra i caratteri. |
| [get_StrikeThrough](./get_strikethrough/)() | True se il font è formattato come testo barrato. |
| [get_Style](./get_style/)() | Ottiene o imposta lo stile del carattere applicato a questa formattazione. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile del carattere applicato a questa formattazione. |
| [get_StyleName](./get_stylename/)() | Ottiene o imposta il nome dello stile del carattere applicato a questa formattazione. |
| [get_Subscript](./get_subscript/)() | True se il font è formattato come pedice. |
| [get_Superscript](./get_superscript/)() | True se il font è formattato come apice. |
| [get_TextEffect](./get_texteffect/)() | Ottiene o imposta l'effetto di animazione del font. |
| [get_ThemeColor](./get_themecolor/)() | Ottiene o imposta il colore del tema nello schema colori applicato associato a questo oggetto [Font](./). |
| [get_ThemeFont](./get_themefont/)() | Ottiene o imposta il font del tema nello schema font applicato associato a questo oggetto [Font](./). |
| [get_ThemeFontAscii](./get_themefontascii/)() | Ottiene o imposta il font del tema usato per il testo latino (caratteri con codici da 0 (zero) a 127) nello schema font applicato associato a questo oggetto [Font](./). |
| [get_ThemeFontBi](./get_themefontbi/)() | Ottiene o imposta il font del tema nello schema font applicato associato a questo oggetto [Font](./) in un documento in lingua da destra a sinistra. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Ottiene o imposta il font del tema dell'Est asiatico nello schema font applicato associato a questo oggetto [Font](./). |
| [get_ThemeFontOther](./get_themefontother/)() | Ottiene o imposta il carattere del tema usato per i caratteri con codici da 128 a 255 nello schema di caratteri applicato associato a questo oggetto [Font](./). |
| [get_TintAndShade](./get_tintandshade/)() | Ottiene o imposta un valore double che schiarisce o scurisce un colore. |
| [get_Underline](./get_underline/)() | Ottiene o imposta il tipo di sottolineatura applicata al carattere. |
| [get_UnderlineColor](./get_underlinecolor/)() | Ottiene o imposta il colore della sottolineatura applicata al carattere. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Verifica se è applicato un determinato effetto di testo DrawingML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Impostatore per [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Impostatore per [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Impostatore per [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Impostatore per [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Impostatore per [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Impostatore per [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Impostatore per [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Impostatore per [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Impostatore per [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Impostatore per [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Impostatore per [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Impostatore per [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Impostatore per [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Impostatore per [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Impostatore per [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Impostatore per [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Impostatore per [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Impostatore per [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Impostatore per [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Impostatore per [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Impostatore per [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Impostatore per [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Impostatore per [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Impostatore per [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Impostatore per [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Impostatore per [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Impostatore per [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Impostatore per [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Impostatore per [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Specifica se il font corrente deve utilizzare le impostazioni di caratteri per riga della griglia del documento durante il layout. |
| [set_Spacing](./set_spacing/)(double) | Impostatore per [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Impostatore per [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Impostatore per [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Impostatore per [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Impostatore per [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Impostatore per [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Impostatore per [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Impostatore per [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Impostatore per [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Impostatore per [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Impostatore per [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Impostatore per [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Impostatore per [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Impostatore per [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Impostatore per [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Impostatore per [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Note


Non si creano istanze della classe [Font](./) direttamente. Si utilizza semplicemente [Font](./) per accedere alle proprietà del carattere dei vari oggetti come [Run](../run/), [Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).

## Esempi



Mostra come inserire una stringa circondata da un bordo in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Mostra come formattare un run di testo usando la sua proprietà font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea uno stile di paragrafo personalizzato.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea un elenco e assicurati che i paragrafi che usano questo stile lo utilizzino.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Applica lo stile di paragrafo al paragrafo corrente del document builder, quindi aggiungi del testo.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifica lo stile del DocumentBuilder in uno che non abbia formattazione di elenco e scrivi un altro paragrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
