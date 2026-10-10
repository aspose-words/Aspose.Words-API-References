---
title: "Aspose::Words::NumberStyle enum"
linktitle: "NumberStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NumberStyle enum. Specifica lo stile numerico per un elenco, note a piè di pagina e note di chiusura, numeri di pagina in C++."
type: docs
weight: 103000
url: /it/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Specifica lo stile di numerazione per un elenco, note a piè di pagina e note finali, numeri di pagina.

```cpp
enum class NumberStyle
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Arabo | 0 | Numerazione araba (1, 2, 3, ...) |
| UppercaseRoman | 1 | Romani maiuscoli (I, II, III, ...) |
| LowercaseRoman | 2 | Romani minuscoli (i, ii, iii, ...) |
| UppercaseLetter | 3 | Lettere maiuscole (A, B, C, ...) |
| LowercaseLetter | 4 | Lettere minuscole (a, b, c, ...) |
| Ordinal | 5 | Ordinal (1°, 2°, 3°, ...) |
| Number | 6 | Numerati (Uno, Due, Tre, ...) |
| OrdinalText | 7 | Ordinal (testo) (Primo, Secondo, Terzo, ...) |
| Esadecimale | 8 | Esadecimale: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Manuale di Chicago di [Style](../style/): *, †, † |
| Kanji | 10 | Ideogramma-digitale. |
| KanjiDigit | 11 | Conteggio giapponese. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Arabo a larghezza piena: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Arabo a mezza larghezza: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Legale giapponese. |
| KanjiTraditional2 | 17 | Diecimila digitale giapponese. |
| NumberInCircle | 18 | Cerchi racchiusi. |
| DecimalFullWidth | 19 | Larghezza piena decimale: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo a larghezza piena. |
| Iroha | 21 | Iroha a larghezza piena. |
| LeadingZero | 22 | Zero iniziale (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Punto (controlla il codice carattere nel testo) |
| Ganada | 24 | Ganada coreano. |
| Chosung | 25 | Corea Chosung. |
| GB1 | 26 | Punto finale racchiuso. |
| GB2 | 27 | Parentesi racchiusa. |
| GB3 | 28 | Cerchio cinese racchiuso. |
| GB4 | 29 | Ideogramma cerchio racchiuso. |
| Zodiac1 | 30 | Ideogramma tradizionale. |
| Zodiac2 | 31 | Ideogramma Zodiaco. |
| Zodiac3 | 32 | Ideogramma Zodiaco tradizionale. |
| TradChinNum1 | 33 | Conteggio taiwanese. |
| TradChinNum2 | 34 | Ideogramma legale tradizionale. |
| TradChinNum3 | 35 | Conteggio taiwanese migliaia. |
| TradChinNum4 | 36 | Digitale taiwanese. |
| SimpChinNum1 | 37 | Conteggio cinese. |
| SimpChinNum2 | 38 | Cinese legale semplificato. |
| SimpChinNum3 | 39 | Conteggio cinese migliaia. |
| SimpChinNum4 | 40 | Cinese (non implementato) |
| HanjaRead | 41 | Digitale coreano. |
| HanjaReadDigit | 42 | Conteggio coreano. |
| Hangul | 43 | Legale coreano. |
| Hanja | 44 | Corea digitale2. |
| Hebrew1 | 45 | Ebraico-1. |
| Arabic1 | 46 | Alfa arabo. |
| Hebrew2 | 47 | Ebraico-2. |
| Arabic2 | 48 | Abjad arabo. |
| HindiLetter1 | 49 | Vocali hindi. |
| HindiLetter2 | 50 | Consonanti Hindi. |
| HindiArabic | 51 | Numeri Hindi. |
| HindiCardinalText | 52 | Descrizione Hindi (cardinali) |
| ThaiLetter | 53 | Lettere Thai. |
| ThaiArabic | 54 | Numeri Thai. |
| ThaiCardinalText | 55 | Descrizione Thai (cardinali) |
| VietCardinalText | 56 | Descrizione vietnamita (cardinali) |
| NumberInDash | 57 | Formato numero di pagina: - 1 -, - 2 -, - 3 -, - 4 -. |
| LowercaseRussian | 58 | Alfabeto russo minuscolo. |
| UppercaseRussian | 59 | Alfabeto russo maiuscolo. |
| None | 255 | Nessun punto elenco o numero. |
| Personalizzato | 65280 | Formato numerico personalizzato. È supportato solo dal formato DOCX. |


## Esempi



Mostra come applicare la formattazione di elenchi personalizzati ai paragrafi quando si utilizza [DocumentBuilder](../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello Microsoft Word e personalizza i primi due livelli dell'elenco.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Questo valore NumberFormat creerà simboli di elenco puntato a forma di stella.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Crea paragrafi e applica entrambi i livelli dell'elenco della nostra formattazione personalizzata a essi.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
